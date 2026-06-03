# DevOps

## Description

DevOps notes for CI/CD, Kubernetes, infrastructure as code, environment promotion, release workflows, automation, and operational checklists.

## Common Commands

```bash
kubectl version --client
kubectl get pods
kubectl get services
terraform version
terraform plan
terraform apply
```

## Examples

Check Kubernetes resources:

```bash
kubectl get all
```

Run a Terraform plan:

```bash
terraform init
terraform plan
```

## Troubleshooting

- Kubernetes context is wrong: check `kubectl config current-context`.
- CI job fails locally but not in CI: compare environment variables, runtime versions, and working directory.
- Terraform plan changes unexpected resources: inspect state, provider versions, and variable files.

## References

- [Kubernetes Documentation](https://kubernetes.io/docs/)
- [Terraform Documentation](https://developer.hashicorp.com/terraform/docs)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
