# ArgoCD Migration Simulation

Repo simulasi untuk `https://github.com/RiziqStankovic/argocd-migration-sim.git`.

Struktur dibuat mirip pola GitOps asli:

- `aws/green/app-of-apps` sebagai root app AWS.
- `aws/etc-cluster-config` sebagai baseline child AWS.
- `aws/cls-log-test` sebagai workload test AWS.
- `tencent/prod/repo-cluster-config` sebagai root app Tencent.
- `tencent/prod/workload/cls-log-test` sebagai workload test Tencent.
- `tencent/cls-test` sebagai workload test tambahan.

Semua workload memakai chart dummy `echo-app` berbasis `nginx`, aman untuk cluster lokal.

## Push ke GitHub

```bash
cd /mnt/d/x/argocd-migration-sim
git init
git add .
git commit -m "Initial ArgoCD migration simulation"
git branch -M master
git remote add origin https://github.com/RiziqStankovic/argocd-migration-sim.git
git push -u origin master
```
