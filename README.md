# Formation sur les outils DevOps (2 jours) — Dépôt de TP

Projet fil rouge : application Java Spring Boot → CI Jenkins → image Docker → déploiement Ansible / Compose / Kubernetes → supervision Prometheus/Grafana + logs ELK.

- **Infrastructure** : [`Vagrantfile`](Vagrantfile) (5 VM Ubuntu 22.04 + provisionnement complet)

## Démarrage rapide

```bash
vagrant up                    # ci + target (jour 1)
vagrant up elk monitor k8s    # jour 2
```

| VM | IP | RAM par défaut | Variable |
|---|---|---|---|
| ci | 192.168.56.10 | 4096 | `CI_RAM` |
| target | 192.168.56.11 | 2048 | `TARGET_RAM` |
| monitor | 192.168.56.12 | 2048 | `MONITOR_RAM` |
| elk | 192.168.56.13 | 4608 | `ELK_RAM` |
| k8s | 192.168.56.14 | 3072 | `K8S_RAM` |

Total si tout tourne : ~16 Go. Jour 1 seul : ~6 Go.



