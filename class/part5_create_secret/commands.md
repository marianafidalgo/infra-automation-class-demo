### Creating a Docker Registry Secret

Use the following command to create a Kubernetes secret for accessing a Docker registry:

```bash
kubectl create secret docker-registry ghcr-secret \
    --docker-server=ghcr.io \
    --docker-username=<your-github-username> \
    --docker-password=<your-github-personal-access-token> \
    --docker-email=<your-email-address> \
    -n <your-namespace>
```

#### Parameters:
- `<your-github-username>`: Replace with your GitHub username.
- `<your-github-personal-access-token>`: Replace with your GitHub Personal Access Token (PAT).
- `<your-email-address>`: Replace with your email address.
- `<your-namespace>`: Replace with the Kubernetes namespace where the secret should be created.

#### Example:
```bash
kubectl create secret docker-registry ghcr-secret \
    --docker-server=ghcr.io \
    --docker-username=johndoe \
    --docker-password=ghp_exampleToken12345 \
    --docker-email=johndoe@example.com \
    -n my-namespace
```
