# 🛠️ Mini-Projet Ansible – Déploiement Serveur 

Ce projet est une initiation pratique à Ansible pour automatiser la configuration d’un serveur Ubuntu.

## 🚀 Objectifs

- Créer un utilisateur `deploy` avec sudo
- Installer et activer `nginx`
- Configurer le pare-feu `ufw` (ouverture des ports 22 et 80)
- Déployer un message de bienvenue personnalisé dans `/etc/motd`

## 📁 Structure du projet
```markdown
├── inventory
├── README.md
├── roles
│   └── server_setup
│       ├── files
│       │   └── motd.txt
│       ├── tasks
│       │   └── main.yml
│       └── vars
│           └── main.yml
├── site.yml
└── Vagrantfile
```
## 🔧 Usage

```bash
ansible-playbook -i inventory site.yml
```
## 📦 Prérequis

- Ansible installé sur le noeud de contrôle (ansible-master)

- Connexion SSH fonctionnelle avec node1 via clé SSH (~/.ssh/id_ansible)

- Accès sudo sans mot de passe pour l'utilisateur vagrant sur le noeud cible


## 🧱 Vagrantfile

Ce projet inclut un fichier `Vagrantfile` pour démarrer automatiquement les machines virtuelles nécessaires au test du playbook.

Lancez-les avec :

```bash
vagrant up
```
