# AfricaOutSource — Landing page (refonte 2026)

Landing page statique (HTML/CSS/JS, sans framework ni dépendance de build) présentant AfricaOutSource : mise en relation entre freelances du digital et entreprises/porteurs de projet en Côte d'Ivoire, avec vérification des profils et paiement sécurisé.

## ⚠️ À faire avant mise en ligne / partage sur les réseaux

Le fichier `index.html` contient des espaces réservés clairement marqués `<!-- TODO -->` à remplacer avant de publier le lien publiquement :

| Élément | Où | Remplacer par |
| --- | --- | --- |
| Lien groupe WhatsApp | Nav (bouton "Rejoindre"), section Communauté | Le vrai lien d'invitation `https://chat.whatsapp.com/...` |
| Numéro WhatsApp contact | Section Contact | Le vrai lien `https://wa.me/225XXXXXXXXXX` |
| E-mail | Section Contact, footer | La vraie adresse (ex. `contact@africaoutsource.com` si elle existe déjà, sinon une adresse surveillée) |
| Réseaux sociaux (footer) | `<a href="#">` LinkedIn / Instagram / TikTok | Les vraies URLs de vos comptes |
| `og:url` / `canonical` | `<head>` | L'URL réelle une fois le site déployé (ex. lien GitHub Pages) |

Les deux boutons "Je suis freelance" / "Je porte un projet" pointent déjà vers vos formulaires Google Forms existants — pas besoin d'y toucher sauf si vous voulez basculer vers un vrai formulaire plus tard.

## Structure

```
index.html          Page unique
css/styles.css       Design system (variables, composants)
js/scripts.js        Nav mobile, scroll, animations d'apparition
assets/              Logo + favicon
```

Aucune dépendance de build : c'est du HTML/CSS/JS pur, servi tel quel.

## Déployer gratuitement avec GitHub Pages

1. Créez un dépôt sur GitHub (ex. `africaoutsource-landing`), public.
2. Poussez ce dossier tel quel (voir commandes ci-dessous).
3. Dans le dépôt GitHub : **Settings → Pages → Branch : `main` / dossier `/root`** → Save.
4. GitHub vous donne une URL du type `https://votre-compte.github.io/africaoutsource-landing/` — c'est ce lien que vous partagez sur les réseaux.
5. (Optionnel) Si vous avez un nom de domaine, ajoutez-le dans Settings → Pages → Custom domain.

```bash
cd africaoutsource-landing
git init
git add .
git commit -m "Landing page AfricaOutSource — refonte 2026"
git branch -M main
git remote add origin https://github.com/VOTRE-COMPTE/africaoutsource-landing.git
git push -u origin main
```

## Ce qui a changé par rapport à la version 2023

- Remplacement du template générique (photo de stock d'accessoires, formulaire de contact non fonctionnel, liens sociaux morts, copyright 2023) par un design propre à la marque.
- Message recentré sur l'hypothèse de marché validée en interne : la confiance et le paiement sécurisé, pas seulement "trouver des talents".
- Formulaire de contact retiré (il ne fonctionnait pas sans jeton payant startbootstrap) au profit de canaux directs réels : WhatsApp, e-mail, formulaires Google déjà utilisés.
- Statistiques honnêtes : plus de faux "+1000 freelancers", des objectifs affichés comme objectifs (cohérent avec la phase de validation en cours).
- Poids de page divisé par ~30 : suppression des visuels génériques (photo d'accessoires en cuir, portraits stock non utilisés) au profit d'un visuel vectoriel léger et animé.
- Site responsive, accessible (focus visible, lien d'évitement, `prefers-reduced-motion` respecté), et fonctionnel même si le JavaScript ne charge pas.
