# L'Auguste Recycleur — Site + Decap CMS (GitHub Pages)

## Structure du projet

```
/
├── index.html                        ← site complet (style + structure)
├── admin/
│   ├── index.html                    ← interface admin (ne pas modifier)
│   └── config.yml                    ← configuration CMS ← À CONFIGURER
├── content/
│   ├── stats.json                    ← chiffres clés (tonnes, personnes, taux)
│   ├── actualites/
│   │   ├── atelier-reparation.json
│   │   ├── collecte-solidaire.json
│   │   └── projet-tiny-house.json
│   └── vitrine/
│       ├── fauteuil-vintage.json
│       ├── radio-bakelite.json
│       ├── velo-ville.json
│       └── lampe-industrielle.json
└── images/                           ← photos uploadées via le CMS
```

---

## Mise en place (à faire une seule fois)

### 1. Créer le repo GitHub
- Créer un repo **public** sur GitHub
- Activer GitHub Pages : Settings → Pages → Source : branche `main`

### 2. Créer une OAuth App GitHub
- Aller sur : GitHub → Settings → Developer Settings → OAuth Apps → New OAuth App
- **Application name** : Auguste Recycleur CMS
- **Homepage URL** : `https://TON-PSEUDO.github.io/TON-REPO`
- **Authorization callback URL** : `https://TON-PSEUDO.github.io/TON-REPO/admin`
- Cliquer sur **Register application**
- Copier le **Client ID** affiché

### 3. Mettre à jour admin/config.yml
Remplacer les deux lignes :
```yaml
repo: TON-PSEUDO/TON-REPO
app_id: TON-CLIENT-ID-GITHUB
```

### 4. Pousser les fichiers sur GitHub
Déposer tous les fichiers à la racine du repo.

### 5. Accéder à l'interface admin
Aller sur : `https://TON-PSEUDO.github.io/TON-REPO/admin`
Se connecter avec son compte GitHub.

---

## Ce qui est éditable via /admin
| Section | Ce qu'on peut modifier |
|---|---|
| Chiffres clés | Tonnes, personnes accompagnées, taux de réemploi |
| Actualités | Ajouter / modifier / supprimer des événements |
| Vitrine du mois | Articles avec photo, prix, badge, description |

## Ce qui se modifie directement dans index.html
- Navigation, services, engagements, contact, footer
- Tout ce qui ne change pas souvent
