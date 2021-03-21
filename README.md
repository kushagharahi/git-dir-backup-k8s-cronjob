# git-dir-backup-k8s-cronjob
Backup a volume to git via Kubernetes CronJob

Setup your volume under the name `git`. This CronJob will commit everything in that volume to the specified Git server. `.gitattributes` recommended if using Git as binary storage.

Setup:
- Fill out env variables

| Env Variable | Description |
| - | - |
| SSH-KEY | Base64 encoded git ssh key |
| GIT-REPO | Upstream git repo ssh uri |
| GIT-EMAIL | Git email |
| GIT-NAME | Git name |
| GIT-BRANCH | Git branch to commit to |
| GIT-COMMIT-MSG | Git commit msg |
- Mount volume under the name `git`
