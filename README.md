# Calculateur de Prix - Impression 3D

Application web autonome pour estimer le coût de revient et le prix de vente de pièces imprimées en 3D.

## Fonctionnalités

### 🧮 Onglet Calcul
- Ajout de pièces avec nom, matériau, poids (g) et temps d'impression (h)
- Raccourcis vers des modèles prédéfinis (Benchy, support téléphone, figurine...)
- Calcul automatique : coût matière, électricité, main d'œuvre, marge, prix total
- Tableau récapitulatif avec totaux
- Récapitulatif visuel par catégorie
- Export CSV du devis
- Suppression individuelle ou de toutes les pièces

### ⚙️ Onglet Configuration
- Prix des matériaux au kg (PLA, PETG, ABS, TPU, ASA, PC, Nylon, Résine)
- Paramètres machine : puissance, coût électricité, puissance lit chauffant
- Marge & frais : pourcentage de marge, frais fixes, coût horaire main d'œuvre, post-traitement
- Gestion des modèles prédéfinis (ajout, modification, suppression)
- Sauvegarde automatique dans le navigateur (localStorage)

## Formule de calcul

```
Coût matière = (Poids en g / 1000) × Prix du matériau au kg
Coût électricité = (Puissance machine + Puissance lit) / 1000 × Temps × Prix kWh
Coût main d'œuvre = Temps × Taux horaire
Coût avant marge = Matière + Électricité + Main d'œuvre + Frais fixes + Post-traitement
Marge = Coût avant marge × (Pourcentage marge / 100)
Prix total = Coût avant marge + Marge
```

## Utilisation

1. Ouvrir `index.html` dans un navigateur web
2. Configurer les paramètres dans l'onglet **Configuration**
3. Ajouter des pièces dans l'onglet **Calcul**
4. Exporter le devis en CSV si besoin

## Technologies

- HTML5 / CSS3 / JavaScript vanilla
- Aucune dépendance externe
- Données persistées via localStorage
- Interface responsive

## Auteur

© 2026 **Grégory HARGOUS** — Tous droits réservés.
