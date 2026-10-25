# AAC — Travaux pratiques

**Algorithmique avancée et complexité** · Master IA et Master RSD
Cours & TD : Dr. Benyamina Ahmed · TP : Mahkouka Mohamed Fouad

*English version below.*

---

## 📂 Une branche par TP

Chaque TP est publié sur sa **propre branche**. La branche `main` contient le TP 0.

| Branche | Contenu |
|---|---|
| `main` | TP 0 — Introduction (Python, VS Code, Git) et TP 0 bis |
| `tp1` | TP 1 — Découverte expérimentale de la complexité |

Les notebooks existent en français (`_FR`) et en anglais (`_EN`).

## 🔀 Changer de branche

### Première fois : cloner le dépôt

```bash
git clone https://github.com/F0u4d8/AAC-TP.git
cd AAC-TP
```

### Voir les branches disponibles

```bash
git fetch                # récupère les nouvelles branches publiées
git branch -a            # liste toutes les branches
```

Les branches distantes apparaissent sous la forme `remotes/origin/tp1`.

### Passer sur une branche

```bash
git switch tp1           # aller sur le TP 1
git switch main          # revenir sur le TP 0
```

> La première fois, `git switch tp1` crée automatiquement la branche locale `tp1` à partir de `origin/tp1`.
> Avec une ancienne version de Git, utilisez `git checkout tp1`.

### Récupérer les mises à jour d'un TP

```bash
git switch tp1
git pull
```

### Vérifier sur quelle branche vous êtes

```bash
git branch               # la branche courante est marquée d'une *
git status               # première ligne : « Sur la branche tp1 »
```

### ⚠️ Avant de changer de branche

Git refuse de changer de branche si vous avez modifié un fichier du dépôt. Deux solutions :

- **Recommandé** : ne modifiez pas les notebooks ici. Copiez le notebook du TP dans **votre propre dépôt** `aac-tp` et travaillez-y.
- Sinon, mettez vos modifications de côté, puis récupérez-les :

```bash
git stash                # met vos modifications de côté
git switch tp1
git stash pop            # les remet en place (si besoin)
```

### Dans VS Code

Cliquez sur le **nom de la branche** en bas à gauche de la fenêtre, puis choisissez la branche dans la liste (`origin/tp1` la première fois).

### Sur GitHub (sans Git)

Sur la page du dépôt, cliquez sur le bouton **`main`** en haut à gauche de la liste des fichiers, choisissez `tp1`, puis ouvrez le notebook et cliquez sur **Download raw file**.

---

# English version

## 📂 One branch per lab

Each lab is published on its **own branch**. The `main` branch holds Lab 0.

| Branch | Content |
|---|---|
| `main` | Lab 0 — Introduction (Python, VS Code, Git) and Lab 0 bis |
| `tp1` | Lab 1 — Experimental discovery of complexity |

Notebooks exist in French (`_FR`) and English (`_EN`).

## 🔀 Switching branches

```bash
git clone https://github.com/F0u4d8/AAC-TP.git   # first time only
cd AAC-TP

git fetch                # get newly published branches
git branch -a            # list all branches

git switch tp1           # go to Lab 1 (use `git checkout tp1` on old Git versions)
git switch main          # back to Lab 0

git pull                 # get updates for the current branch
git branch               # the current branch is marked with *
```

**Before switching:** Git refuses to switch if you changed a file in this repository. Work on a copy of the notebook in **your own** `aac-tp` repository, or run `git stash` before switching and `git stash pop` afterwards.

**VS Code:** click the **branch name** at the bottom left of the window, then pick the branch (`origin/tp1` the first time).

**GitHub (no Git):** click the **`main`** button above the file list, pick `tp1`, open the notebook and click **Download raw file**.
