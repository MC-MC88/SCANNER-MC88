# 📷 Scanner MC88 — Lecteur QR & Code-Barres

**Scanner MC88** est un scanner de QR codes et de codes-barres professionnel qui fonctionne entièrement dans votre navigateur. Il propose trois modes de numérisation : caméra en direct, prise de photo via l'appareil photo natif, et téléchargement d'image existante. Tout le décodage est effectué localement sur votre appareil.

---

## 📋 Prérequis

1. Un navigateur web moderne (Chrome, Firefox, Edge, Safari, Brave, Opera)
2. Pour le mode **caméra en direct** : connexion sécurisée (`https://` ou `localhost`)
3. Pour **Prendre une photo** et **Télécharger une image** : aucun prérequis spécial
4. Aucune installation de logiciel nécessaire

---

## 🚀 Guide d'installation

### Étape 1 : Télécharger le fichier

1. Téléchargez le fichier `scanner-mc88.html` sur votre ordinateur
2. Placez-le dans un dossier de votre choix

### Étape 2 : Lancer l'application

**Méthode simple (fonctionnalités photo/upload) :**
- Double-cliquez sur le fichier
- Les modes **Prendre une photo** et **Télécharger une image** fonctionnent immédiatement

**Pour le mode caméra en direct (nécessite HTTPS) :**
- Utilisez un serveur local : VS Code Live Server, Python `http.server`, etc.
- Ou hébergez le fichier sur un site HTTPS (GitHub Pages, Netlify, Vercel…)
- Le mode caméra est bloqué par les navigateurs sur `file://` pour des raisons de sécurité

---

## 🎯 Guide d'utilisation détaillé

### 🔹 Étape 1 : Choisir un mode de numérisation

L'application propose **3 modes** :

#### 📹 Mode Caméra en Direct
1. Cliquez sur l'onglet **"Live Camera"**
2. Cliquez sur **"Enable Camera"** pour autoriser l'accès
3. Choisissez la caméra (avant/arrière) dans le menu déroulant
4. Cliquez sur **"Start Camera"**
5. Alignez le code dans le cadre de visée

#### 📸 Mode Prendre une Photo
1. Cliquez sur l'onglet **"Take Photo"**
2. Cliquez sur la zone de capture
3. L'appareil photo natif de votre téléphone s'ouvre
4. Prenez la photo (utilisez le zoom si nécessaire)
5. Le scan se fait automatiquement

#### 📤 Mode Télécharger une Image
1. Cliquez sur l'onglet **"Upload Image"**
2. Cliquez sur la zone de téléchargement
3. Choisissez une image existante contenant un code
4. Le scan se fait automatiquement

---

### 🔹 Étape 2 : Lire le résultat

Après un scan réussi, le panneau de résultat affiche :

| Élément | Description |
|---------|-------------|
| **Badge** | Type de code détecté (QR_CODE, EAN_13, CODE_128…) |
| **Texte** | Le contenu décodé complet |
| **Actions** | Boutons contextuels selon le type de contenu |

**Actions intelligentes selon le contenu :**

| Type | Actions disponibles |
|------|---------------------|
| **URL** | Ouvrir dans un nouvel onglet, Copier |
| **Email** | Envoyer un email, Copier |
| **Téléphone** | Appeler, Copier |
| **Wi-Fi** | Copier le mot de passe (avec infos réseau) |
| **vCard** | Enregistrer le contact (.vcf), Copier |
| **Texte/Code-barres** | Rechercher en ligne, Copier |

---

### 🔹 Étape 3 : Configurer les options

| Option | Description |
|--------|-------------|
| **Beep on scan** | Joue un son à chaque scan réussi |
| **Vibrate on scan** | Vibre à chaque scan (mobile uniquement) |
| **Auto-open links** | Ouvre automatiquement les URLs (désactivé par défaut) |
| **Save history** | Enregistre l'historique des scans |

---

### 🔹 Étape 4 : Utiliser la lampe torche

1. Cliquez sur l'icône **éclair** ⚡
2. Active la lampe torche de votre appareil
3. Utile pour scanner dans l'obscurité
4. Support dépendant de l'appareil

---

## 📊 Formats supportés

| Format | Type | Description |
|--------|------|-------------|
| **QR Code** | 2D | Le plus courant |
| **Aztec** | 2D | Billets, documents |
| **Data Matrix** | 2D | Industriel, composants |
| **PDF 417** | 2D | Cartes d'identité, transport |
| **Code 128** | 1D | Logistique, emballages |
| **Code 39** | 1D | Industriel, militaire |
| **Code 93** | 1D | Compact, sécurité |
| **Codabar** | 1D | Bibliothèques, sang |
| **EAN-13** | 1D | Produits européens |
| **EAN-8** | 1D | Petits produits |
| **UPC-A** | 1D | Produits américains |
| **UPC-E** | 1D | Produits compacts |
| **ITF** | 1D | Cartons, emballages |

---

## 🛠️ Guide de dépannage

### Problème 1 : La caméra ne démarre pas

**Cause** : Le fichier est ouvert en `file://` (pas de connexion sécurisée).

**Solution** :
- Utilisez les modes **Prendre une photo** ou **Télécharger une image**
- Ou lancez un serveur local (VS Code Live Server)
- Ou hébergez le fichier sur HTTPS (GitHub Pages)

---

### Problème 2 : La bibliothèque de scan ne charge pas

**Cause** : Script bloqué par un bloqueur de publicité ou connexion faible.

**Solution** :
- Désactivez temporairement votre bloqueur de publicité
- Vérifiez votre connexion Internet
- Rechargez la page (F5)
- Le bouton **"Tap to retry"** apparaît si la bibliothèque échoue

---

### Problème 3 : Le code ne se scanne pas

**Cause** : Mauvais éclairage, flou, ou code trop petit.

**Solution** :
- Utilisez le mode **Prendre une photo** avec le zoom natif
- Rapprochez-vous du code
- Assurez-vous que le code est bien éclairé
- Essayez un angle différent

---

### Problème 4 : La lampe torche ne fonctionne pas

**Cause** : L'appareil ne supporte pas le contrôle de la torche via le navigateur.

**Solution** :
- Utilisez la torche manuelle de votre téléphone
- Essayez un autre navigateur (Chrome mobile)
- Certains appareils iOS ne supportent pas cette fonction

---

### Problème 5 : L'historique ne se sauvegarde pas

**Cause** : Le stockage local est désactivé ou en navigation privée.

**Solution** :
- Vérifiez que le stockage local est activé
- En navigation privée, l'historique sera réinitialisé
- C'est un comportement normal

---

### Problème 6 : Les liens ne s'ouvrent pas automatiquement

**Cause** : L'option "Auto-open links" est désactivée (par défaut).

**Solution** :
- Activez l'option dans les paramètres
- Ou cliquez sur **"Open in New Tab"** manuellement
- La désactivation par défaut est une mesure de sécurité

---

## 📋 Historique des scans

- **50 scans** maximum sauvegardés
- Stockage local persistant
- Cliquez sur un élément pour le réafficher
- Bouton **✕** pour supprimer un élément
- Bouton **"Clear history"** pour tout effacer

---

## 🔒 Confidentialité

- **100% local** : Le décodage s'effectue entièrement dans votre navigateur
- **Aucune donnée envoyée** : Aucune image ni résultat ne quitte votre appareil
- **Aucun cookie** : Pas de suivi
- **Stockage local** : Seul l'historique est sauvegardé localement

---

## 📄 Copyright

**© 2026**  
📧 mohamed005cheikh@gmail.com  
**Créé par MC88**  
**Tous droits réservés**

---

## 🔗 Bibliothèque utilisée

- **html5-qrcode** v2.3.8 : Bibliothèque de décodage QR/barcode
- Chargée depuis CDN avec fallback automatique
- Supporte tous les formats listés ci-dessus

---

## ✅ Fonctionnalités techniques

- **3 modes de scan** : caméra, photo, upload
- **13 formats** de codes supportés
- **Torche** intégrée (si supportée)
- **Actions intelligentes** selon le contenu
- **Historique persistant** (50 entrées)
- **Beep et vibration** configurables
- **Détection de type** : URL, email, téléphone, Wi-Fi, vCard
- **Design responsive** mobile-first
- **Animations** de balayage et de logo
- **Fallback CDN** automatique

---

**Bon scan ! 📷✨**
