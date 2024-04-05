# Docker
This repository contains resources and examples related to Docker, a Type-1 virtualization platform that simplifies the management of application processes in containers. Containers allow applications to run in isolation, while using a single system kernel. Here you will find instructions on how to install Docker on Windows and Ubuntu,

Installation et configuration de Docker sur Windows  
---------------------------------------------------

Il existe principalement deux manières d’installer Docker sur Windows:

Installation interactive : Cette méthode utilise l’interface utilisateur graphique (GUI) pour installer Docker. Vous téléchargez Docker Desktop à partir du site officiel de Docker, puis vous exécutez le fichier d’installation et suivez les instructions à l’écran.

Installation à partir de la ligne de commande : Cette méthode est plus technique et nécessite l’utilisation de l’invite de commandes (CMD). Vous téléchargez le fichier d’installation de Docker Desktop, puis vous utilisez l’invite de commandes pour exécuter le fichier d’installation.

Pour le téléchargement de Docker Desktop : Rendez-vous sur le site officiel de Docker à l’adresse https://www.docker.com/products/docker-desktop et téléchargez Docker Desktop pour Windows.


Installation et configuration de maniere interactive
----------------------------------------------------

### Installation 

Téléchargez le programme d'installation à l'aide du bouton de téléchargement en haut de la page ou à partir des notes de version .

Double-cliquez Docker "Desktop Installer.exe" pour exécuter le programme d'installation. Par défaut, Docker Desktop est installé sur C:\Program Files\Docker\Docker.

Lorsque vous y êtes invité, assurez-vous que l' option Utiliser WSL 2 au lieu d'Hyper-V sur la page de configuration est sélectionnée ou non en fonction de votre choix de backend.

Si votre système ne prend en charge qu'une des deux options, vous ne pourrez pas sélectionner le backend à utiliser.

Suivez les instructions de l'assistant d'installation pour autoriser le programme d'installation et poursuivre l'installation.

Une fois l'installation réussie, sélectionnez Fermer pour terminer le processus d'installation.

### Configuration 

Si votre compte administrateur est différent de votre compte utilisateur, vous devez ajouter l'utilisateur au groupe docker-users :

Exécutez la gestion de l'ordinateur en tant qu'administrateur .
Accédez à Utilisateurs et groupes locaux > Groupes > docker-users .
Cliquez avec le bouton droit pour ajouter l'utilisateur au groupe.
Déconnectez-vous et reconnectez-vous pour que les modifications prennent effet.


Si Docker Desktop ne démarre pas automatiquement après l'installation.
Pour démarrer Docker Desktop :
Recherchez Docker et sélectionnez Docker Desktop dans les résultats de la recherche.

Si Docker Desktop se lance automatiquement :
Vous pouvez accéder aux paramètres de Docker en cliquant avec le bouton droit de la souris sur l’icône de Docker dans la barre des tâches et en sélectionnant “Settings”.


Installation et configuration via une invite de commandes
----------------------------------------------------------

### Installation 

Après le téléchargement Docker Desktop Installer.exe, exécutez la commande suivante dans un terminal pour installer Docker Desktop :
 "Docker Desktop Installer.exe" install

Si vous utilisez PowerShell, vous devez l'exécuter comme :
Start-Process 'Docker Desktop Installer.exe' -Wait install

Si vous utilisez l'invite de commande Windows :
start /w "" "Docker Desktop Installer.exe" install
Par défaut, Docker Desktop est installé sur C:\Program Files\Docker\Docker.

La install commande accepte les indicateurs suivants :

--quiet: Supprime la sortie d'informations lors de l'exécution du programme d'installation

--accept-license : accepte le contrat de service d'abonnement Docker  maintenant, plutôt que d'exiger qu'il soit accepté lors de la première exécution de l'application

--no-windows-containers: Désactive l'intégration des conteneurs Windows

--allowed-org=<org name> : nécessite que l'utilisateur se connecte et fasse partie de l'organisation Docker Hub spécifiée lors de l'exécution de l'application

--backend=<backend name>: sélectionne le backend par défaut à utiliser pour Docker Desktop, hyper-vou windows( wsl-2par défaut)

--installation-dir=<path>: modifie l'emplacement d'installation par défaut ( C:\Program Files\Docker\Docker)


### Configuration 

--admin-settings: crée automatiquement un admin-settings.jsonfichier qui est utilisé par les administrateurs pour contrôler certains paramètres de Docker Desktop sur les machines clientes au sein de leur organisation. Pour plus d'informations, voir Gestion des paramètres .

Il doit être utilisé avec le --allowed-org=<org name>drapeau.
Par exemple : --allowed-org=<org name> --admin-settings='{"configurationFileVersion": 2, "enhancedContainerIsolation": {"value": true, "locked": false}}'

--proxy-http-mode=<mode>: Définit le mode proxy HTTP system(par défaut) oumanual

--override-proxy-http=<URL>: Définit l'URL du proxy HTTP qui doit être utilisé pour les requêtes HTTP sortantes, nécessite --proxy-http-moded'êtremanual

--override-proxy-https=<URL>: Définit l'URL du proxy HTTP qui doit être utilisé pour les requêtes HTTPS sortantes, nécessite --proxy-http-moded'êtremanual

--override-proxy-exclude=<hosts/domains>: contourne les paramètres de proxy pour les hôtes et les domaines. Utilise une liste séparée par des virgules.

--hyper-v-default-data-root=<path>: Spécifie l'emplacement par défaut du disque de la machine virtuelle Hyper-V.

--windows-containers-default-data-root=<path>: Spécifie l'emplacement par défaut des conteneurs Windows.

--wsl-default-data-root=<path>: Spécifie l'emplacement par défaut du disque de distribution WSL.

--always-run-service: permet aux utilisateurs de basculer vers des conteneurs Windows sans avoir besoin de droits d'administrateur.

Note
----
Si vous utilisez PowerShell, vous devez utiliser le ArgumentListparamètre avant tout indicateur.
Par exemple: Start-Process 'Docker Desktop Installer.exe' -Wait -ArgumentList 'install', '--accept-license'

Si votre compte administrateur est différent de votre compte utilisateur, vous devez ajouter l'utilisateur au groupe docker-users :
 net localgroup docker-users <user> /add


# Autor #
<div style="display:flex;align-items:center">

<div style="display:flex;align-items:center">
    <div>
        <h5> <a href='https://github.com/KongaDan'>Konga Dan</a> </h5>
        <h5> <a href='https://github.com/JulioIlunga'>Ilunga Elie</a> </h5>
        <h5> <a href='https://github.com/Lygie-Furaha'>Furaha Lygie</a> </h5>
        <h5> <a href='https://github.com/Marisel4'>Lisangola Sarah</a> </h5>
        <h5> <a href=''>Lubamba Divin</a> </h5>
        <h5> <a href='https://github.com/MolishoTheProgrammer'>Molisho Christian</a> </h5>
<div>
    
</div>
