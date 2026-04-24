# 🚀 Edge Gateway

## 📌 Visão Geral

O **Edge Gateway** é o projeto responsável pela camada de entrada dos serviços publicados no ambiente de infraestrutura.

Sua principal finalidade é atuar como **Reverse Proxy corporativo**, centralizando o acesso web aos sistemas internos e externos por meio de URLs amigáveis, segurança, organização e escalabilidade.

Este projeto foi concebido para ambientes baseados em **Docker Swarm**, utilizando **Nginx** como proxy reverso principal e integração com **GitLab CI/CD** para automação de deploys.

---

## 🎯 Objetivos do Projeto

- Centralizar o acesso aos serviços web da infraestrutura
- Publicar aplicações através de domínios e subdomínios
- Padronizar entrada HTTP / HTTPS
- Facilitar manutenção e crescimento do ambiente
- Permitir deploy automatizado via pipeline
- Isolar serviços internos da exposição direta
- Melhorar organização da arquitetura

---

## 🏗️ Arquitetura Base

- Usuário
   ↓
- DNS Interno / Público
   ↓
- Edge Gateway (Nginx Reverse Proxy)
   ↓
- Serviços Internos
   ├── Portainer
   ├── GitLab
   ├── Aplicações Docker
   ├── Sistemas Web
   └── APIs

🛠️ Tecnologias Utilizadas

- Infraestrutura
- Docker Engine
- Docker Swarm
- Overlay Networks
- Linux Debian / Ubuntu
- Proxy / Web
- Nginx
- SSL / TLS
- Virtual Hosts
- Load Balancing (futuro)
- DevOps
- GitLab
- GitLab Runner
- GitLab CI/CD
- Segurança
- Reverse Proxy Segregado
- Headers HTTP
- TLS Certificates
- Isolamento de Containers

📁 Estrutura do Projeto

- edge-gateway/
- conf.d/            # Virtual hosts / domínios
- certs/             # Certificados SSL
- logs/              # Logs do nginx
- nginx.conf         # Configuração principal
- stack.yml          # Deploy Docker Swarm
- .gitlab-ci.yml     # Pipeline CI/CD
- README.md          # Arquivo de documentação

🌐 Exemplos de Publicação

- portainer.lab.gomes.local
- git.seduc.lab.gomes.local
- app.seduc.lab.gomes.local
- api.seduc.lab.gomes.local

⚙️ Modelo Operacional

- Alteração em arquivos do projeto
- Commit no GitLab
- Pipeline executa automaticamente
- Docker Swarm atualiza stack
- Nginx recarrega nova configuração

🔐 Segurança Prevista

- TLS / HTTPS
- Headers de segurança
- Controle de exposição de portas
- Segmentação de rede Docker
- Logs centralizados

📈 Evoluções Futuras

- Let's Encrypt automático
- WAF
- Rate Limit
- Geo Blocking
- Monitoramento
- Alta disponibilidade avançada
- Métricas Prometheus

💻 Administração

Projeto mantido para estudos avançados de infraestrutura, redes, containers e DevOps.

Ambiente focado em laboratório realista com boas práticas corporativas.

🚀 Edge Gateway

Camada inteligente de entrada para serviços modernos.

---
*Mantido por Ricardo Gomes Infraestrutura e Redes - lab.gomes.local*
