# tenant-b-apps — Tenant B applications (demo-env)

GitOps repository for **tenant-b** namespace workloads on demo-env.

Synced by the platform `ApplicationSet` in [ocp-platform](https://github.com/YOUR_GITHUB_ORG/ocp-platform) (`charts/tenant-onboarding`).

## Layout

```
deploy/
├── Chart.yaml
├── values.yaml
└── templates/
    ├── deployment.yaml
    ├── service.yaml
    └── route.yaml
```

## Local validation

```bash
helm lint deploy
helm template tenant-b deploy -f deploy/values.yaml --namespace tenant-b
```

## Ownership

- Namespace: `tenant-b`
- Argo CD AppProject: `tenant-b`
- Owner group: `tenant-b-owners`

## Related repositories

- [ocp-bootstrap](https://github.com/YOUR_GITHUB_ORG/ocp-bootstrap) — IdP and RBAC for tenant-b-owner
- [ocp-platform](https://github.com/YOUR_GITHUB_ORG/ocp-platform) — ApplicationSet entry for this repo
