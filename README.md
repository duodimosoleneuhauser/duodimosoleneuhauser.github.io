# Site du Duo Di Mosole–Neuhauser

Site statique hébergé sur GitHub Pages, domaine `duodimosoleneuhauser.com` (fichier `CNAME`).

## Structure

| Fichier / dossier | Rôle |
|---|---|
| `index.html` | Page d’accueil (toutes les sections, fenêtres de la discographie, scripts) |
| `concerts.html` | Archives de scène |
| `presse.html` | Revue de presse |
| `mentions-legales.html` | Mentions légales |
| `404.html` | Page d’erreur personnalisée |
| `img/` | Images optimisées pour le web (à utiliser dans les pages) |
| `img/presse/` | Photo haute définition proposée au téléchargement |
| `docs/` | Dossiers artistiques PDF proposés au téléchargement |
| `_sources/originaux/` | Fichiers sources en pleine résolution, **non publiés** (dossier ignoré par GitHub Pages) |
| `robots.txt`, `sitemap.xml` | Référencement |

## Ajouter ou remplacer une image

Les navigateurs n’ont pas besoin de photos de plusieurs mégaoctets. Tailles cibles :

- Photo d’accueil : 1600 px de large (`img/duo-concert-1600.jpg`) et 960 px pour le téléphone.
- Pochettes d’album : 480 px de côté.
- Affiches et articles : 1000 px sur le plus grand côté.

Sur Mac, sans rien installer, dans le Terminal :

```bash
sips -Z 1000 -s format jpeg -s formatOptions 75 "affiche-originale.jpg" --out img/affiche-1000.jpg
```

Placez l’original dans `_sources/originaux/` et référencez la version `img/` dans la page, avec les attributs `width`, `height` et `loading="lazy"`.

## Annoncer un concert

Dans `index.html`, section `id="concerts"` : remplacer l’affiche, la date (`.concert-date`), le titre (`h3`) et le texte. Pour un concert à venir, écrire « Prochain concert • date » à la place de « Dernier concert ». Ajouter ensuite le lieu dans la liste de `concerts.html`.

## Mettre à jour la date du plan du site

Après une modification importante, mettre à jour `lastmod` dans `sitemap.xml`.
