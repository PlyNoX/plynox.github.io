# Commandes Linux

1. [Commandes de base](#commandes-de-base)
   1.1. [Créations](#créations)
   1.2. [Renommer](#renommer)
   1.3. [Suppression](#suppression)
   1.4. [Affichages des dossiers/fichiers](#affichages-des-dossiersfichiers)
   1.5. [Déplacements](#déplacements)

2. [Compression / Décompression](#compression--décompression)

3. [Autres](#autres)
   3.1. [Réseau](#réseau)
   3.2. [Commandes associées à John the Ripper](#commandes-associées-à-john-the-ripper)
   3.3. [Brute force](#brute-force)
   3.4. [Stéganographie](#stéganographie)
   3.5. [Mots de passe utiles](#mots-de-passe-utiles)
   3.6. [Liens utiles](#liens-utiles)
   3.7. [Commandes pour trouver des fichiers avec des droits spécifiques](#commandes-pour-trouver-des-fichiers-avec-des-droits-spécifiques)

4. [Réseau](#réseau)

5. [Commandes pour trouver des fichiers avec des droits spécifiques](#commandes-pour-trouver-des-fichiers-avec-des-droits-spécifiques)

6. [Notes](#notes)

## Commandes de base
### Créations
- **Créer un dossier :** `mkdir [nom]`
- **Créer un fichier :** `touch [nom]`
- **Déplacer :** `mv [ancien_chemin] [nouveau_chemin]`

### Renommer
- `mv [ancien_nom] [nouveau_nom]`

### Suppression
- **Supprimer des fichiers/dossiers :** `rm`
- **Supprimer dossier plein :** `rm -rf [nom]`
- **Supprimer dossier vide :** `rmdir [nom]`
- **Supprimer fichier :** `rm [nom]`
- `rm -r` (recursive), `rm -i` (confirmation)

### Affichages des dossiers/fichiers
- **Contenu du dossier :** `ls`
- **Contenu du dossier + fichiers cachés :** `ls -a`
- **Contenu du dossier + permissions :** `ls -l`
- **Contenu du dossier + fichiers cachés + permissions :** `ls -la`

### Déplacements
- **Changer de répertoire :** `cd [nom]`
- **Retourner sur HOME :** `cd` ou `cd ~`
- **Retourner dans le dossier précédent :** `cd -` ou `cd ..`
- **Savoir son emplacement :** `pwd`

## Compression / Décompression
- `tar`
- `gzip`
- `unzip`
- `gunzip`
- `bzip2`

## Autres
- **Auto-complétion :** TAB
- **Répéter la dernière commande :** `!!`
- **Annuler/Abandonner :** `Ctrl C`
- **Installer :** `sudo apt-get install [nom]`
- **Nettoyer le Terminal :** `clear`
- **Lancer le Terminal :** `Ctrl Alt T`
- **Fermer le Terminal :** `exit`
- **Commande précédente :** flèche du haut
- **Commande suivante :** flèche du bas
- **Pour voir les tâches planifiées :** `cat crontab`
- **Resort tous les caractères alphanumériques sans les caractères spéciaux :** `grep :`

## Réseau
- `ifconfig` or `ip`: Afficher les informations sur les interfaces réseau.
- `ping`: Tester la connectivité réseau.
- `ping exemple.com`: Vérifier la connectivité avec un domaine.
- **Pour savoir quelle droit a l’utilisateur :** `sudo -l`

## Commandes associées à John the Ripper
- `zip2john`
- `rar2john`
- `pdf2john`
- `gpg2john`
- `racf2john`
- `keepass2john`
- `office2john`

## Brute force
- `hydra` (brute force pour mdp)
  - `hydra -l [name] -P /usr/share/wordlists/rockyou.txt [IPV4] [ftp]`

- `john` (brute force pour hash)
  - `john --wordlist=/usr/share/wordlists/rockyou.txt [hashfile]`

## Stéganographie
- **Steghide :** `steghide extract -sf fichier.jpeg`
- **Stegcracker :** `stegcracker fichier.jpeg [chemin_wordlist]`

## Mots de passe utiles
- **Tryhackme FTP :** `anonymous / anonymous`

## Liens utiles
- [Liste des commandes basiques sur Kali Linux](https://wordpress.com/view/web.lmd.jussieu.fr/~flott/polytechnique/mec583_08/linux_vi_f77.pdf)
- [Reverse Shell Cheatsheet](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md)
- [Exemples de hash](https://hashcat.net/wiki/doku.php?id=example_hashes)

## Commandes pour trouver des fichiers avec des droits spécifiques
- `find / -perm -u=s -ls 2>/dev/null`
- `find / -type f -perm -04000 -ls 2>/dev/null`
- `find / -type f -perm -u=s -ls 2>/dev/null`

## Réseau
- `ifconfig` or `ip`: Afficher les informations sur les interfaces réseau.
- `ping`: Tester la connectivité réseau.
- `ping exemple.com`: Vérifier la connectivité avec un domaine.

## Commandes pour trouver des fichiers avec des droits spécifiques
- `find / -perm -u=s -ls 2>/dev/null`
- `find / -type f -perm -04000 -ls 2>/dev/null`
- `find / -type f -perm -u=s -ls 2>/dev/null`

## Notes
La liste de commandes Linux est extensive. Il est recommandé de les pratiquer dans un environnement sécurisé.
