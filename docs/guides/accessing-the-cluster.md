# Accessing the Kubernetes Cluster

## 1. Prerequisites

Ensure you have `kubectl` installed.

```bash
sudo apt-get update
sudo apt-get install -y kubectl
```

This configuration uses OIDC (OpenID Connect) for authentication via Keycloak. To access the cluster, you must have the `oidc-login` plugin installed.

If you have Krew installed, this is the most reliable method:
```bash
kubectl krew install oidc-login
```

---

## 2. Set up the config file

Below YAML is the configuration file that you need to connect to the cluster. By default, Kubectl will look for this file in `~/.kube/config`.

```yaml
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM2akNDQWRLZ0F3SUJBZ0lCQURBTkJna3Foa2lHOXcwQkFRc0ZBREFWTVJNd0VRWURWUVFERXdwcmRXSmwKY201bGRHVnpNQjRYRFRJMU1UQXdOakl4TkRFeE1Gb1hEVE0xTVRBd05ESXhORFl4TUZvd0ZURVRNQkVHQTFVRQpBeE1LYTNWaVpYSnVaWFJsY3pDQ0FTSXdEUVlKS29aSWh2Y05BUUVCQlFBRGdnRVBBRENDQVFvQ2dnRUJBTFdDCnFsMXl6b1RGOGVuSFMwalA1SXFtN3JhYWtaZzMvcFJpd0hjTWFPTDZBQUFkdGpEMWNMRkVpQ1EwRzdpN1lIVEwKMmxTd0FNanUvYXN5WXRNMWV5Nzc1K2J2UzM2V2Z4ajlmUTZ6NXBDR0I5eExqRzVnSG5rWURYRGFrVlI2bGl1ZApQM0lpemthOXFPTzBVdmpEVGh2TDRPd3Z0dUtKV0VFM0RYcXpMcmJvVmF4RmdROFY3ZmVnWDJUcXJBWEZ5SS83Cnk4RlliTWJMRUJvdHh3V3RnTXlGMlllQ09pT2VOTCt4cnAyQjZ5aGV5ZG8zQmJzRkNPY3RhQTFIV1dqQ3BHc0kKWWUvcFVYRlVNU29DMkpMM2toK3k3UTFia1ZpUm9jaHBEY3VaQUxpbUUxaTBZdEdST0d0bW9QdDdEaFBkNnJNcwpxeUNsemFCdk53NFJmRmo3UzY4Q0F3RUFBYU5GTUVNd0RnWURWUjBQQVFIL0JBUURBZ0trTUJJR0ExVWRFd0VCCi93UUlNQVlCQWY4Q0FRQXdIUVlEVlIwT0JCWUVGTEI4TEVuWTRJZFpMdExkY3lkNjNiQlcwalVNTUEwR0NTcUcKU0liM0RRRUJDd1VBQTRJQkFRQTRwSFQ1ZnV1aUZTTkJhUmlLRFpyRE5Nc0tNbmdUTGhJTHdpT3pXQk11NGd3MgpRQ3c3N0xWcTBHbWhENG5iQmUvNjI3dkhjeEVKV1NBd25jYUZvQ09zNzFIVkhBUnBMRks5SXN6VkdVZjlYOG1vCkdJeTVMbnBvcGRlU0NUa3hjSk5oUU1QNURlMjhvYThlUEU0K0prRFM5Q3dPWTVVSDBPY204RElKalphWjhYUy8KZmxYNXFJNHgvOXRtZnQ0M3d4Vk4zS25VMVJtSjhSUzFNSFZkNDdwWE5ZUTBqY2hrNEtyYkM1T2t6T1dBMktFNwpPZXBPTS9VUGlsVG1DR1owMENNNGFWVW8yMCsxQUU2aVRIWVdnNndxUHhwVHBxRGorUko1bXJzb2QrcWJ2NUR3CncxQlNyNVRXbFRMbVRCMlZSc0JUWFc2Ri8rSXFGUFdtQTRrcno2UHoKLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
    server: https://163.7.145.113:6443
  name: capi131-drai-ai-test
contexts:
- context:
    cluster: capi131-drai-ai-test
    user: oidc
  name: capi131-drai-ai-test
current-context: capi131-drai-ai-test
kind: Config
preferences: {}
users:
- name: oidc
  user:
    exec:
      apiVersion: client.authentication.k8s.io/v1
      args:
      - oidc-login
      - get-token
      - --oidc-issuer-url=https://keycloak.test.drai.auckland.ac.nz/realms/drai
      - --oidc-client-id=k8s-test
      - --oidc-client-secret=0JgSbpmVgvqNpjxn5u5ExcMeLpGCcRYi
      - --oidc-extra-scope=groups
      command: kubectl
      env: null
      interactiveMode: Never
      provideClusterInfo: false
```

---

## 3. Connecting to the Cluster

Upon running your first `kubectl` command:

1. A browser window will automatically open loading the Keycloak login page.
2. Log in with your standard credentials.
3. Once authenticated, the browser will display "You are logged in," and your terminal command will execute.

Here are some useful commands to get started:

```bash
kubectl get pods -n kai-test
kubectl get services -n kai-test
```

---

## Caveats

At this stage, we are still working on the Tuakiri integration, and only able to provide you access if you already have an account with us. Please reach out to jun.huh@auckland.ac.nz if you would like to request an account.