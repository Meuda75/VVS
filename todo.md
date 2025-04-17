TODO: Importer l’ancienne version du site

Salut ! Voici les étapes à suivre pour uploader ton ancienne version du site (en fichier .zip) dans une branche séparée.
🔧 1. Installer Git (si ce n’est pas encore fait)
Sur Mac :

    Ouvre le Terminal (tu peux le trouver via Spotlight avec Cmd + Espace, puis tape “Terminal”).

    Tape git et appuie sur Entrée.

    Si Git n’est pas installé, macOS va te proposer de l’installer automatiquement. Accepte.

Sur Windows :

    Va sur https://git-scm.com

    Télécharge et installe Git avec les options par défaut.

🔄 2. Mettre à jour ton fork

Dans ton terminal, tape les commandes suivantes :

### Cloner ton propre fork (si tu ne l’as pas déjà fait)

    git clone https://github.com/Meuda75/VVS.git

    cd VVS

### Ajouter le repo original comme remote "upstream"

    git remote add upstream https://github.com/vascoII/VVS.git

### Mettre à jour ta copie locale avec la version la plus récente du repo original

    git fetch upstream
    git merge upstream/main

🌿 3. Créer une nouvelle branche

    git checkout -b import-ancien-site

📦 4. Ajouter ton fichier ZIP

    Glisse-dépose le fichier .zip de ton ancien site dans le dossier du repo (ou utilise l’Explorateur/Finder).

    Si tu as plusieurs fichiers .zip, ajoute-les tous maintenant.

💾 5. Commit et push

    git add .

    git commit -m "Ajout ancienne version du site"

    git push origin import-ancien-site

✅ C’est tout ! Préviens-moi quand c’est fait, je récupérerai ta branche pour m’en occuper.
Merci ! 🙌
