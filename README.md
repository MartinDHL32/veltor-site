# 🚀 Veltor - Site Vitrine

Site web professionnel pour Veltor, entreprise de conception web, développement d'applications et CRM pour PME/TPE.

![Veltor](images/logo_veltor.png)

---

## 📁 Structure du projet

```
veltor-site/
├── index.html          # Page principale
├── css/
│   └── style.css       # Styles CSS
├── js/
│   └── main.js         # JavaScript (interactions)
├── images/
│   ├── logo_veltor.svg # Logo SVG
│   ├── logo_veltor.png # Logo PNG
│   ├── projet-1.jpg    # Image projet 1 (à ajouter)
│   ├── projet-2.jpg    # Image projet 2 (à ajouter)
│   ├── projet-3.jpg    # Image projet 3 (à ajouter)
│   └── projet-4.jpg    # Image projet 4 (à ajouter)
└── README.md           # Ce fichier
```

---

## 🖼️ Ajouter vos images de projets

Pour afficher vos réalisations, ajoutez vos images dans le dossier `images/` avec les noms suivants :

- `projet-1.jpg` - Image du projet 1 (E-commerce Mode)
- `projet-2.jpg` - Image du projet 2 (App Restaurant)
- `projet-3.jpg` - Image du projet 3 (CRM Immobilier)
- `projet-4.jpg` - Image du projet 4 (Cabinet Avocats)

**Recommandations pour les images :**
- Format : JPG ou PNG
- Taille recommandée : 1200x800 pixels minimum
- Ratio : 3:2 ou 16:9
- Poids : < 500 Ko (optimisez avec [TinyPNG](https://tinypng.com/))

---

## 💻 Installation locale avec Visual Studio Code

### Prérequis
- [Visual Studio Code](https://code.visualstudio.com/) installé
- [Git](https://git-scm.com/) installé
- Extension "Live Server" pour VS Code (recommandé)

### Étapes

1. **Ouvrir le dossier dans VS Code**
   ```bash
   # Décompressez le fichier ZIP puis :
   cd veltor-site
   code .
   ```

2. **Installer l'extension Live Server**
   - Ouvrez VS Code
   - Allez dans Extensions (Ctrl+Shift+X)
   - Recherchez "Live Server"
   - Installez l'extension de Ritwick Dey

3. **Lancer le site en local**
   - Clic droit sur `index.html`
   - Sélectionnez "Open with Live Server"
   - Le site s'ouvre à `http://127.0.0.1:5500`

---

## 📤 Déploiement sur GitHub

### 1. Créer un compte GitHub (si nécessaire)
Allez sur [github.com](https://github.com) et créez un compte.

### 2. Créer un nouveau repository

1. Cliquez sur le bouton vert "New" sur GitHub
2. Nom du repository : `veltor-site`
3. Description : "Site vitrine Veltor"
4. Laissez en "Public"
5. **NE cochez PAS** "Add a README file"
6. Cliquez sur "Create repository"

### 3. Initialiser Git et pousser le code

Ouvrez le terminal dans VS Code (Ctrl+`) et exécutez :

```bash
# Initialiser Git dans le projet
git init

# Ajouter tous les fichiers
git add .

# Créer le premier commit
git commit -m "Initial commit - Site Veltor"

# Connecter au repository GitHub (remplacez VOTRE_USERNAME)
git remote add origin https://github.com/VOTRE_USERNAME/veltor-site.git

# Renommer la branche en 'main'
git branch -M main

# Pousser le code sur GitHub
git push -u origin main
```

### 4. Vérifier sur GitHub
Rafraîchissez la page de votre repository sur GitHub. Vos fichiers devraient apparaître.

---

## 🌐 Déploiement sur Vercel

### 1. Créer un compte Vercel

1. Allez sur [vercel.com](https://vercel.com)
2. Cliquez sur "Sign Up"
3. Choisissez "Continue with GitHub"
4. Autorisez Vercel à accéder à votre compte GitHub

### 2. Importer le projet

1. Sur le dashboard Vercel, cliquez sur "Add New..." > "Project"
2. Dans la liste de vos repositories, trouvez `veltor-site`
3. Cliquez sur "Import"

### 3. Configurer le déploiement

Sur l'écran de configuration :

- **Project Name** : `veltor` (ou laissez par défaut)
- **Framework Preset** : "Other" (détecté automatiquement)
- **Root Directory** : `.` (racine, laissez par défaut)
- **Build Command** : (laissez vide)
- **Output Directory** : `.` (laissez par défaut)

Cliquez sur "Deploy"

### 4. Votre site est en ligne ! 🎉

Après quelques secondes, Vercel vous donnera une URL comme :
`https://veltor-site.vercel.app`

---

## 🔄 Mettre à jour le site

Après avoir fait des modifications :

```bash
# Ajouter les changements
git add .

# Créer un commit
git commit -m "Description de vos modifications"

# Pousser sur GitHub
git push
```

**Vercel redéploiera automatiquement !** Chaque `git push` déclenche un nouveau déploiement.

---

## 🌍 Configurer un nom de domaine personnalisé

### Sur Vercel :

1. Allez dans votre projet sur Vercel
2. Cliquez sur "Settings" > "Domains"
3. Ajoutez votre domaine : `veltor.fr`
4. Vercel vous donnera des enregistrements DNS à configurer

### Chez votre registrar (OVH, Gandi, etc.) :

Ajoutez ces enregistrements DNS :
```
Type A     : @ -> 76.76.21.21
Type CNAME : www -> cname.vercel-dns.com
```

Attendez la propagation DNS (jusqu'à 48h).

---

## 📝 Personnalisations à faire

### Informations à modifier dans `index.html` :

1. **Email** (ligne ~450) : Remplacez `contact@veltor.fr`
2. **Téléphone** (ligne ~460) : Remplacez `+33 6 00 00 00 00`
3. **Liens réseaux sociaux** (footer) : Ajoutez vos vrais liens
4. **Statistiques** (hero) : Ajustez les chiffres selon vos vraies stats

### Couleurs (dans `css/style.css`) :

Si vous souhaitez modifier les couleurs, éditez ces variables en haut du fichier :
```css
:root {
    --primary-blue: #5B6EF4;
    --primary-purple: #8B5CF6;
    /* ... */
}
```

---

## 📧 Configurer le formulaire de contact

Le formulaire est actuellement en mode "simulation". Pour le rendre fonctionnel :

### Option 1 : Formspree (gratuit, simple)

1. Inscrivez-vous sur [formspree.io](https://formspree.io)
2. Créez un nouveau formulaire
3. Modifiez l'attribut `action` du formulaire dans `index.html` :
```html
<form class="contact-form" id="contact-form" action="https://formspree.io/f/VOTRE_ID" method="POST">
```

### Option 2 : Netlify Forms

Si vous déployez sur Netlify au lieu de Vercel, ajoutez simplement :
```html
<form class="contact-form" id="contact-form" netlify>
```

---

## 🛠️ Technologies utilisées

- **HTML5** - Structure
- **CSS3** - Styles & animations
- **JavaScript** (Vanilla) - Interactions
- **Google Fonts** - Space Grotesk, JetBrains Mono
- **Vercel** - Hébergement

---

## 📱 Responsive Design

Le site est entièrement responsive et optimisé pour :
- 📱 Mobile (< 480px)
- 📱 Tablette (480px - 768px)
- 💻 Laptop (768px - 1024px)
- 🖥️ Desktop (> 1024px)

---

## ⚡ Performance

- Score Lighthouse visé : 90+
- Pas de dépendances externes lourdes
- Images optimisées
- CSS et JS minifiables

---

## 📄 Licence

© 2024 Veltor. Tous droits réservés.

---

## 🆘 Support

Des questions ? Contactez-nous à contact@veltor.fr
