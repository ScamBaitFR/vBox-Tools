# Scam-baiting avec un hôte Windows 10 utilisant VirtualBox d'Oracle.
Version traduite du projet [Scambaiting-Setup de xSerpentineX](https://github.com/xSerpentineX/Scambaiting-Setup).

### A : Qu'est-ce que le scam-baiting ?
Le scam-baiting est l'art de faire perdre du temps à un escroc afin d'éviter que des personnes réelles ne soient affectées par cet escroc. Le scam-baiting peut également s'étendre à des actions plus graves telles que la suppression de fichiers, le verrouillage de l'ordinateur des escrocs, la collecte d'informations sur les escrocs, etc. Bien que ces autres activités soient illégales, les risques de se faire arrêter par la police pour s'être frotté à des escrocs sont plutôt minces. Cependant, il est toujours conseillé de prendre des précautions de base en matière d'anonymat.

### B : Comment puis-je configurer un environnement d'escroquerie avec VirtualBox ?
La mise en place d'un environnement d'appât à escroquerie n'est pas aussi difficile que certaines personnes peuvent le penser. Voici un guide complet sur la façon de le faire :

##### Installer VirtualBox :
Tout d'abord, vous devez installer VirtualBox. Il est recommandé d'utiliser la dernière version. Pour ce faire, [téléchargez VirtualBox ici] (https://www.virtualbox.org/wiki/Downloads).

Une fois le fichier téléchargé, installez-le comme vous le feriez normalement pour un logiciel (par exemple, Windows utilise son assistant d'installation). Après avoir installé VirtualBox, exécutez-le. Vous devriez tomber sur un écran qui ressemble à ceci :

![Nouvel écran de VirtualBox](https://user-images.githubusercontent.com/66549839/87617329-2eb0d880-c70f-11ea-84d7-2503422b3861.png)

---
##### Création d'une nouvelle machine virtuelle :
Lors de la création d'une nouvelle machine virtuelle Windows 10, certains utilisateurs peuvent avoir du mal à la configurer correctement, même après avoir téléchargé leur fichier ISO Windows 10 - la même chose m'est arrivée. Cependant, maintenant que j'ai les connaissances, c'est en fait incroyablement facile, c'est juste que la plupart des utilisateurs débutants ne penseraient pas à le faire. Voici donc comment configurer votre machine virtuelle Windows 10 !
- Téléchargez le [fichier ISO Windows 10] (https://www.microsoft.com/en-us/software-download/windows10ISO).

- Accédez à l'écran principal de l'application VirtualBox et cliquez sur le bouton bleu **Nouveau**.
- Nommez la machine virtuelle comme vous le souhaitez et sélectionnez son type comme Microsoft Windows et sa version comme Windows 10 (64 bits).
- Attribuez à la machine la quantité de RAM que vous souhaitez (personnellement, j'utilise 4 Go de RAM pour mes VM, mais vous pouvez utiliser jusqu'à 2 Go).
- Gardez la sélection : "Créer un disque dur virtuel maintenant", et cliquez sur "Suivant".
- Gardez la sélection : "VDI (VirtualBox Disk Image)", et cliquez sur "Suivant".
- Maintenez la sélection : "Alloué dynamiquement", et cliquez sur "Suivant".
- Donnez à la machine une quantité d'espace <ins>**raisonnable**</ins> (suffisante pour les fichiers du système d'exploitation et votre propre utilisation).
- Après avoir créé la machine, mettez-la en surbrillance en cliquant une fois dessus, puis cliquez sur le bouton orange **Paramètres**.
- Allez dans la section **Stockage** via le panneau de gauche.
- Vous devriez voir une icône de disque qui dit : "Vide". Cliquez dessus pour le mettre en surbrillance.
- Après avoir mis le disque en surbrillance, vous devriez voir sur le panneau de droite une étiquette indiquant : "Attributs". En dessous de cette étiquette, vous devriez voir une autre étiquette qui dit : "Lecteur optique :" avec un menu déroulant à côté. **A côté du menu déroulant, cliquez sur la petite icône de disque bleu, puis sélectionnez : "Choisir un fichier de disque optique virtuel "**.
- Sélectionnez le fichier ISO Windows 10 que vous avez téléchargé précédemment. Après avoir sélectionné le fichier ISO, appuyez sur OK pour fermer la fenêtre des paramètres.
- Mettez en surbrillance la machine virtuelle que vous venez de créer et cliquez sur le bouton vert **Démarrer**. À partir de là, la machine s'allume et commence à installer Windows 10.

---
##### Installation de Windows 10 :
Avant d'installer Windows 10 pour l'escroquerie, il y a quelques considérations importantes dont vous devez tenir compte...
- Lorsque Windows 10 vous demande une clé d'activation, cliquez sur l'option permettant d'activer Windows 10 ultérieurement (ce que, bien entendu, vous ne ferez pas).

- Installez Windows 10 Pro ; il vous donnera accès à regedit.
- **Ne jamais** utiliser vos vraies informations. Lorsque Windows 10 vous demande l'e-mail de votre compte Microsoft, choisissez l'option pour créer un tout nouveau compte outlook. De plus, lorsque Windows 10 vous demande un compte de secours, vous pouvez également utiliser un e-mail aléatoire (par exemple, mon e-mail aléatoire est cle************@protonmail.com) ; mon vrai nom ne commence pas par "cle".
- Refusez toutes les offres et tous les services, qu'il s'agisse de retrouver votre appareil, de connaître votre position, d'utiliser votre voix, etc.
- Lorsque vous définissez le mot de passe de votre compte, **ne définissez pas un mot de passe que vous utilisez pour votre machine hôte ou tout autre service**.
---
### C1 : Déguiser votre machine virtuelle. 
L'une des choses les plus importantes à faire avec une machine virtuelle est de cacher aux escrocs le fait qu'il s'agit d'une machine virtuelle. De nos jours, la plupart des escrocs vérifient si la machine à laquelle ils sont connectés est une machine virtuelle ou non pour voir s'ils sont appâtés et, s'ils découvrent qu'il s'agit d'une machine virtuelle, ils se déconnectent généralement et raccrochent. Vous pouvez déguiser une machine virtuelle Oracle en procédant comme suit :
- [Téléchargez l'outil vBoxSysInfoMod](https://github.com/JayMontana36/vBoxSysInfoMod/). Ensuite, exécutez le fichier `vBox System Info Mod.bat` et suivez les instructions dans le terminal (Pour le fabricant du système, vous pouvez utiliser Dell - pour le modèle du système, vous pouvez utiliser n'importe quel modèle Dell (par exemple Optiplex 745)). **Notez que vous devez arrêter votre machine virtuelle si elle est en cours d'exécution pour éviter toute corruption.**

- Une fois ce processus terminé, vous pouvez prendre les mesures suivantes **dans la machine virtuelle** pour la dissimuler davantage aux escrocs :
  - Lancez `regedit` en utilisant la fenêtre d'exécution (Win+R) et naviguez jusqu'au chemin suivant : HKEY_LOCAL_MACHINE ➡️ SOFTWARE ➡️ Microsoft ➡️  Windows ➡️ CurrentVersion ➡️ Uninstall. Dans ce chemin, vous devriez voir un dossier nommé "Oracle VM VirtualBox Additions". Supprimez ce dossier, car cela empêchera l'escroc de le voir dans `appwiz.csl` (Si le dossier n'existe pas, vous n'avez pas à vous inquiéter !).
  
  - Ensuite, vous devez naviguer vers le chemin suivant : HKEY_LOCAL_MACHINE ➡️ SYSTEM ➡️ ControlSet001. 
  - Dans ce chemin, vous devriez voir un dossier nommé "Enum". Faites un clic droit sur le dossier et cliquez sur : "Permissions". Ensuite, cliquez sur le bouton "Ajouter" et entrez le nom d'utilisateur de votre machine virtuelle dans la zone de texte. Après avoir saisi le nom d'utilisateur, cliquez sur OK. Enfin, allez à l'option que vous venez d'ajouter et cochez : "Autoriser le contrôle total" puis cliquez sur : "Appliquer".
  - À partir de là, cliquez sur le bouton "Avancé". En haut de la fenêtre pop-up, cliquez sur le lien "Modifier" et, à nouveau, entrez le nom d'utilisateur de votre machine virtuelle dans la zone de texte, puis cliquez sur OK. Ensuite, cliquez sur : "Appliquer".
  - Ensuite, ouvrez à nouveau le menu Avancé et cochez la case "Remplacer tous les objets enfants...". Ensuite, cliquez à nouveau sur "Appliquer" et OK (ne vous inquiétez pas si la case est décochée après l'application).
  - Voici la partie fastidieuse. Faites un clic droit sur le dossier "Enum" et cliquez sur "Rechercher". De là, entrez le hash suivant : `4d36e967-e325-11ce-bfc1-08002be10318` et cliquez sur "Rechercher suivant". Maintenant, faites un clic droit sur l'option "FriendlyName", cliquez sur "Modifier" et changez la valeur en "Samsung 50 GB ATA".
  - Ensuite, faites un nouveau clic droit sur le dossier "Enum" et cliquez sur "Rechercher". Entrez le hash suivant : `4d36e968-e325-11ce-bfc1-08002be10318` et modifiez le "DeviceDesc" en "Nvidia Geforce GTX 1080".
  - Ensuite, faites un nouveau clic droit sur le dossier "Enum" et cliquez sur "Rechercher". Entrez le hash suivant : `4d36e965-e325-11ce-bfc1-08002be10318` et modifiez le "FriendlyName" en "NEC DVD-RW SATA DVD01".
  - Enfin, faites à nouveau un clic droit sur le dossier "Enum" et cliquez sur "Rechercher". Entrez le hash suivant : `4d36e96f-e325-11ce-bfc1-08002be10318` et modifiez le "DeviceDesc" en "Microsoft Pointing Device". Maintenant, cliquez deux fois sur F3 et modifiez le "DeviceDesc" suivant en "Microsoft USB Pointing Device".

---
### C2 : Déguisement supplémentaire :
Donc, vous avez changé tous les paramètres compliqués, bon travail ! (**ATTENTION : SI VOUS UTILISEZ LES AJOUTS DE VIRTUALBOX GUEST, FERMEZ LES ICÔNES DE LA BARRE D'ÉTAT SYSTÈME EN UTILISANT LE GESTIONNAIRE DE TÂCHES. DE PLUS, VOUS DEVRIEZ DÉSACTIVER LE GESTIONNAIRE DE TÂCHES ET LE METTRE SUR LE COMPTE D'UN VIRUS. DE PLUS, ÉJECTEZ LE CD DE VIRTUALBOX GUEST ADDITIONS.**)

Cependant, un PC frais aura l'air suspect, alors n'oubliez pas d'utiliser [Ninite](https://ninite.com) pour installer certaines applications dans la machine virtuelle (téléchargez les fichiers sur votre machine virtuelle, pas sur votre hôte).

En outre, vous voudrez également utiliser un fond d'écran personnalisé. **Il existe un moyen simple de le faire sans clé d'activation**. Il suffit de télécharger une image depuis internet sur votre bureau. Ensuite, **déplacez-la** dans le fichier Windows 10 dans le chemin suivant : `C:\Windows\Web\Wallpaper\Windows 10`. Après cela, il suffit de faire un clic droit sur l'image et de cliquer sur "Définir comme fond d'écran". Notez que vous ne pouvez pas ajuster son rognage, choisissez donc une image qui correspond approximativement à la résolution de la machine virtuelle.

#### Avant de sauvegarder un instantané de votre machine virtuelle, vérifiez que vous avez effectué les opérations suivantes :
1. Vous avez réussi à modifier la machine virtuelle à l'aide de l'outil vmSysInfoMod.
2. Vous avez supprimé le dossier Guest Additions de Regedit si vous utilisez Guest Additions.
3. Vous avez réussi à modifier chacune des quatre valeurs de hachage comme indiqué ci-dessus.
4. Vous avez réussi à installer quelques applications pour vous faire passer pour un innocent.
5. Vous avez réussi à changer le fond d'écran pour qu'il corresponde à la personnalité de la prétendue victime.

### Si toutes ces conditions sont remplies, enregistrez un instantané de la machine.
Ceci peut être fait en utilisant le menu supérieur de la fenêtre de Virtual Box : `Machine -> Prendre un instantané`. Ensuite, chaque fois que vous terminez un appât, lorsque vous éteignez la machine, cochez la case "Restaurer à <nom de l'instantané>" pour revenir à cet état de configuration terminé.
