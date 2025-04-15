# Projet Docker DevOps

## Objectif
Ce projet vise à démontrer la capacité à déployer un serveur web Nginx sur un conteneur SSH via Ansible, en utilisant une infrastructure Docker orchestrée par Docker Compose. L'intégration d'un pipeline GitLab CI est également envisagée pour automatiser l'ensemble du processus.

## Structure du projet
- `ansible/` : Contient les rôles et playbooks Ansible.
- `ssh_server/` : Contient le Dockerfile et les configurations pour le serveur SSH.
- `docker-compose.yml` : Fichier d'orchestration des conteneurs Docker.

## Instructions
1. Construisez les images Docker : `docker-compose build`
2. Lancez les conteneurs : `docker-compose up -d`
3. Exécutez le playbook Ansible pour déployer Nginx : `docker exec -it ansible_controller ansible-playbook -i ansible/inventory ansible/playbook.yml`
4. Accédez au serveur web via `http://localhost:8080`

## Remarques
- Assurez-vous que Docker et Docker Compose sont installés sur votre machine.
- Ce projet est conçu pour des environnements Linux (Ubuntu ou CentOS).
