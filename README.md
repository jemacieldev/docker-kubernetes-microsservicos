# Docker e Kubernetes em 3 sistemas operacionais

Trabalho da disciplina **Design de Serviços e Micro-serviços** (Centro Universitário Belas Artes) · Jéssica Maciel da Silva · RA 24215046

O workflow `.github/workflows/docker-kubernetes.yml` demonstra, em máquinas reais do GitHub Actions:

| Job | O que mostra |
|---|---|
| Docker no Linux (Ubuntu) | Instalação oficial pelo repositório apt, `hello-world` e a imagem `nginx` do Docker Hub servindo a pasta `site/` |
| Docker no Windows | Docker Engine com containers Windows e a imagem `hello-world` |
| Docker no macOS | Instalação do cliente com Homebrew e por que o daemon precisa de uma VM |
| Cluster Kubernetes com 3 nós | Cluster `kind` com 1 control-plane e 2 workers, Deployment do NGINX com 3 réplicas, Service e escala para 5 |

## Arquivos

- `k8s/kind-3-nos.yaml` – configuração do cluster com 3 nós
- `k8s/nginx-deployment.yaml` – Deployment com 3 réplicas do NGINX
- `k8s/nginx-service.yaml` – Service do tipo NodePort
- `site/index.html` – página servida pelo container NGINX
