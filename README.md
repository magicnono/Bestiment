# 🏗️ BESTIMENT - Interface Web de Construction

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![WordPress](https://img.shields.io/badge/WordPress-Compatible-blue.svg)

## 📋 Description

Bestiment est une interface web moderne et professionnelle conçue pour les entreprises de construction et de rénovation. Avec un design élégant aux couleurs bleues vives, cette interface offre une expérience utilisateur optimale et est entièrement compatible avec WordPress.

## ✨ Fonctionnalités

- ✅ Design moderne et professionnel
- ✅ Palette de couleurs bleues vives et attrayantes
- ✅ Logo personnalisé avec effet graphique
- ✅ Navigation intuitive et sticky header
- ✅ Section hero avec appel à l'action
- ✅ Grille de services avec animations hover
- ✅ Formulaire de contact stylisé
- ✅ Design 100% responsive (mobile, tablette, desktop)
- ✅ Effets visuels et animations fluides
- ✅ Compatible WordPress

## 🎨 Palette de Couleurs

| Couleur | Hex Code | Utilisation |
|---------|----------|-------------|
| Bleu Principal | `#0096ff` | Éléments principaux, CTA |
| Bleu Foncé | `#0066cc` | Dégradés, accents |
| Bleu Clair | `#00d4ff` | Highlights, effets |
| Noir | `#0a0a0a` | Arrière-plans |
| Gris Foncé | `#1a1a1a` | Cards, sections |
| Blanc | `#ffffff` | Texte principal |

## 📦 Installation

### Installation Directe (HTML)

1. Téléchargez le fichier HTML
2. Ouvrez-le avec votre navigateur web
3. Personnalisez le contenu selon vos besoins

### Installation WordPress

#### Méthode 1 : Page Template

```php
<?php
/*
Template Name: Bestiment Landing Page
*/
?>
<!DOCTYPE html>
<html <?php language_attributes(); ?>>
<head>
    <meta charset="<?php bloginfo('charset'); ?>">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title><?php bloginfo('name'); ?> - Bestiment</title>
    <?php wp_head(); ?>
    
    <!-- Collez le code CSS ici entre les balises <style> -->
</head>
<body>
    <!-- Collez le code HTML du body ici -->
    <?php wp_footer(); ?>
</body>
</html>
```

#### Méthode 2 : Elementor / Page Builder

1. Installez Elementor ou votre page builder préféré
2. Créez une nouvelle page
3. Ajoutez un widget HTML
4. Collez le code HTML complet
5. Ajoutez un widget CSS pour les styles

#### Méthode 3 : Thème Enfant

1. Créez un thème enfant WordPress
2. Ajoutez le fichier `page-bestiment.php`
3. Collez le code dans ce fichier
4. Sélectionnez le template dans l'éditeur de page

## 🛠️ Personnalisation

### Modifier les Couleurs

Recherchez et remplacez les valeurs hexadécimales dans la section CSS :

```css
/* Couleur principale */
#0096ff → Votre nouvelle couleur

/* Couleur secondaire */
#0066cc → Votre nouvelle couleur

/* Couleur d'accent */
#00d4ff → Votre nouvelle couleur
```

### Modifier le Logo

Le logo est créé avec CSS. Pour le personnaliser :

```css
.logo-icon {
    width: 60px; /* Modifier la taille */
    height: 60px;
    background: linear-gradient(135deg, #0096ff 0%, #0066cc 100%);
}
```

### Ajouter des Sections

Suivez la structure HTML existante :

```html
<section class="nouvelle-section">
    <div class="container">
        <h2 class="section-title">Titre de la Section</h2>
        <!-- Votre contenu -->
    </div>
</section>
```

## 📱 Responsive Design

L'interface s'adapte automatiquement aux différentes tailles d'écran :

- **Desktop** : > 768px - Affichage complet
- **Tablette** : 768px - 480px - Navigation simplifiée
- **Mobile** : < 480px - Menu compact, grille adaptative

## 🔧 Configuration du Formulaire

### Avec WordPress

Intégrez avec Contact Form 7 ou WPForms :

```php
<?php echo do_shortcode('[contact-form-7 id="123"]'); ?>
```

### Avec PHP (Traitement basique)

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nom = htmlspecialchars($_POST['nom']);
    $email = htmlspecialchars($_POST['email']);
    $message = htmlspecialchars($_POST['message']);
    
    // Envoi d'email
    $to = "votre@email.com";
    $subject = "Nouveau message de " . $nom;
    $body = "Email: " . $email . "\n\nMessage:\n" . $message;
    
    mail($to, $subject, $body);
}
?>
```

## 🚀 Optimisation

### Performance

- Minifiez le CSS pour la production
- Optimisez les images (si vous en ajoutez)
- Activez la mise en cache WordPress
- Utilisez un CDN pour les ressources

### SEO

```html
<!-- Ajoutez dans le <head> -->
<meta name="description" content="Bestiment - Votre partenaire en construction">
<meta name="keywords" content="construction, rénovation, bâtiment">
<meta property="og:title" content="Bestiment Construction">
<meta property="og:description" content="Excellence en construction">
```

## 📂 Structure des Fichiers

```
bestiment/
│
├── index.html              # Fichier principal
├── README.md              # Documentation
├── css/
│   └── style.css          # Styles (optionnel si séparé)
├── js/
│   └── script.js          # Scripts (optionnel)
└── assets/
    └── images/            # Images du projet
```

## 🆘 Support & FAQ

### Le menu ne s'affiche pas sur mobile ?

Le menu est masqué sur mobile par défaut. Pour ajouter un menu burger, ajoutez ce code JavaScript :

```javascript
// Code pour menu mobile hamburger
document.addEventListener('DOMContentLoaded', function() {
    // Votre code de menu mobile ici
});
```

### Comment changer les icônes des services ?

Remplacez les emojis par des icônes Font Awesome ou autres :

```html
<!-- Au lieu de 🏗️ -->
<i class="fas fa-building"></i>
```

### Le formulaire ne fonctionne pas ?

Assurez-vous d'avoir configuré le traitement PHP ou d'utiliser un plugin WordPress comme Contact Form 7.

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :

1. Fork le projet
2. Créer une branche (`git checkout -b feature/amelioration`)
3. Commit vos changements (`git commit -m 'Ajout d'une fonctionnalité'`)
4. Push vers la branche (`git push origin feature/amelioration`)
5. Ouvrir une Pull Request

## 📝 License

Ce projet est sous licence MIT. Vous êtes libre de l'utiliser, le modifier et le distribuer.

## 👨‍💻 Auteur

Créé pour Bestiment Construction

## 📞 Contact

Pour toute question ou suggestion :

- Email : magicnonogamer@gmail.com
- Site Web : www.bestiment.com

## 🔄 Changelog

### Version 1.0.0 (2026-01-17)
- ✨ Version initiale
- 🎨 Design moderne avec couleurs bleues
- 📱 Interface responsive
- 🏗️ Logo personnalisé
- 📋 Section services
- 📧 Formulaire de contact

---

**⭐ Si ce projet vous plaît, n'oubliez pas de lui donner une étoile !**
