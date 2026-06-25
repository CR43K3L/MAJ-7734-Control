# Updater GitHub - 7734 Control

Repo utilise par l'app:

```txt
https://github.com/CR43K3L/MAJ-7734-Control
```

URL fixe lue par l'app:

```txt
https://raw.githubusercontent.com/CR43K3L/MAJ-7734-Control/main/version.json
```

## Premiere mise en place

1. Mets `version.json` a la racine du repo GitHub.
2. Cree une Release GitHub nommee `v1.0.3`.
3. Ajoute le fichier `installer/7734-Control-Setup-1.0.3.exe` comme fichier de la Release.
4. Envoie une derniere fois le setup `1.0.3` a tes amis.

Pourquoi une derniere fois: les anciennes versions ont une URL de mise a jour vide. La `1.0.3` contient l'URL du repo, donc les prochaines versions pourront se faire depuis l'app.

## Pour les prochaines versions

1. Augmente la version dans l'app, par exemple `1.0.4`.
2. Build le setup.
3. Cree une Release GitHub `v1.0.4`.
4. Upload `7734-Control-Setup-1.0.4.exe` dans cette Release.
5. Modifie le `version.json` a la racine du repo:

```json
{
  "version": "1.0.4",
  "downloadUrl": "https://github.com/CR43K3L/MAJ-7734-Control/releases/download/v1.0.4/7734-Control-Setup-1.0.4.exe",
  "notes": "Notes de mise a jour."
}
```

L'app compare sa version locale avec `version`. Si la version en ligne est plus recente, elle affiche `Installer`, telecharge le setup, le lance, puis ferme l'app.
