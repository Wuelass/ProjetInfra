# Projet Web Apps : WordPress & Wekan (Docker Compose)

Ce projet déploie WordPress et Wekan via Docker Compose, avec Apache comme reverse proxy.

Lien vers le swisstransfer : [Télécharger le projet](https://www.swisstransfer.com/d/331d3411-fd0c-4649-9d7d-f4d0b085bdaf)

## 1. Prérequis & Accès VM

* **Système :** VM Linux (Debian/Ubuntu/CentOS) avec Docker & Docker Compose installés.
* **IP VM :** Notez l'adresse IP de votre VM .
* **Mot de passe VM :** `Wuela`.

## 2. Emplacement des Fichiers

Les fichiers du projet se trouvent dans le répertoire `/web_app/` sur votre VM :

/web_app/
├── docker-compose.yml
└── apache/
├── httpd.conf
└── conf.d/
├── wordpress.conf
└── wekan.conf

## 3. Lancement des Applications (Docker Compose)

1.  Connectez-vous à votre VM.
2.  Naviguez vers `/web_app/`.
3.  Démarrez la stack :
    
    docker compose up -d
    
4.  Vérifiez que tous les services sont `Up` :
    
    docker compose ps
    
5.  Surveillez les logs Apache pour un démarrage propre :
    
    docker compose logs -f apache

## 4. Voir le Résultat

Ouvrez un navigateur sur votre **PC hôte** et accédez aux applications via l'IP de votre VM :

* **WordPress :** `http://<IP_de_votre_VM>/`
    
* **Wekan :** `http://<IP_de_votre_VM>/wekan/`
    

