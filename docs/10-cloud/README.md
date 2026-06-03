# Cloud

## Description

Cloud notes for AWS, Azure, and Google Cloud Platform, including CLI setup, authentication, storage, networking, compute, databases, and deployment workflows.

## Common Commands

```bash
aws --version
aws sts get-caller-identity
az version
az account show
gcloud version
gcloud auth list
```

## Examples

Verify AWS identity:

```bash
aws sts get-caller-identity
```

List Google Cloud projects:

```bash
gcloud projects list
```

## Troubleshooting

- CLI is authenticated to the wrong account: inspect the active profile, subscription, or project.
- Permission denied: verify IAM role, policy, subscription role, or service account permissions.
- Region mismatch: confirm the configured region and resource location.

## References

- [AWS Documentation](https://docs.aws.amazon.com/)
- [Azure Documentation](https://learn.microsoft.com/azure/)
- [Google Cloud Documentation](https://cloud.google.com/docs)
