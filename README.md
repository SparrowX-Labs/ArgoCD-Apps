# Argo CD applications

GitOps application definitions for the SparrowX EKS platform. The `dev/` and `prod/` trees contain separate Argo CD projects, root applications, application-of-applications manifests, and environment values.

The two environments run as namespaces on the same EKS cluster. Argo CD reads application resources from the corresponding environment directory and deploys the shared Helm charts from `Custom-Apps-HelmCharts` and `EKS-HelmCharts`.

## Layout

- `dev/` and `prod/`: environment-specific Argo CD resources.
- `applications/`: customer-facing service applications.
- `infrastructure/`: Crossplane, External Secrets, and platform integrations.
- `internal-platform/`: Backstage and the Python action service.
- `app-of-apps/`: Argo CD child-application composition.

Apply the environment project and root application with Argo CD or `kubectl` after the cluster platform components are available.

## License

See [LICENSE.md](LICENSE.md).
