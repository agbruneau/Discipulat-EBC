# CLAUDE.md — `Recherches/`

Recherches exégétiques de l'épître de **Jacques**, une par péricope (12 semaines de
prédication), pour l'**Église Baptiste de Charlesbourg**. Voir le `README.md` racine pour
la vue d'ensemble et la table des passages. Ce fichier ne couvre que ce qui n'est pas
dérivable du dépôt.

## Cadre théologique — non négociable

Tout le contenu doit être **impérativement conforme à la théologie de John MacArthur**
(Master's Seminary), cadre baptiste réformé. Le skill `oia-reformee` est la grille de
référence : l'invoquer avant toute analyse ou correction doctrinale.

Décision éditoriale arrêtée : **« trancher pour MacArthur »**. Concrètement :

- **Eschatologie / Israël-Église** (priorité absolue) : la lecture **dispensationaliste
  prémillénariste prétribulationniste** de MacArthur *conclut* chaque divergence. La lecture
  covenantale/amillénariste de la 1689 peut être signalée honnêtement mais reste **nettement
  subordonnée** — « témoin minoritaire », jamais à parité, jamais le dernier mot. Ne jamais
  spiritualiser/allégoriser les promesses faites à Israël.
- **Sotériologie** : monergisme (TULIP), *sola fide* + double imputation, persévérance des
  saints, **Lordship Salvation** (foi et repentance indissociables ; pas de croyant
  non-disciple). Aucun glissement *easy-believism* / Free Grace / régénération décisionnelle.
- **Jacques 2** : « la foi seule sauve, mais la foi qui sauve n'est jamais seule ». Les œuvres
  **démontrent** la foi, elles ne justifient pas devant Dieu. Réfuter toute justification *par*
  les œuvres (NPP, sacramentalisme).
- **Cessationnisme strict** : pour Jacques 5.14-15, l'onction = soin pastoral ordinaire et
  prière de la foi, **ni** guérison charismatique **ni** extrême-onction sacramentelle.
- Témoins reçus sur la sotériologie/providence/christologie (Calvin, Spurgeon, les puritains,
  Schreiner) : à conserver sur ces sujets, **jamais** comme autorité covenantale-amillénariste
  co-équivalente sur l'eschatologie.

**Ne jamais inventer de citation de MacArthur** ni de référence non vérifiable. Paraphraser
ses positions documentées.

## Structure d'un dossier

Chaque `Jacques-c-vv-vv/` contient trois fichiers à garder cohérents :

| Fichier | Rôle |
|---|---|
| `Recherche-Exegetique-Jacques-*.md` | **source** rédigée (prose continue) |
| `index.html` | **rendu** pour le web, applique le gabarit visuel de `../../Syntheses-Globales/index.html` |
| `Recherche-Exegetique-Jacques-*.pdf` | **export** paginé du `.md`, imprimable |

Gabarit d'une recherche (7 sections) : Contexte · Arrière-plan historique et culturel ·
Étude des mots-clés (tableau : translittération, sens, champ sémantique, traductions S21/
NEG79/Darby/LSG/KJF) · Apports des commentateurs (MacArthur, Calvin, 1689) · Renvois et
passages parallèles · Thèmes théologiques (« Dans le texte » + « Pour votre assemblée ») ·
Pistes de réflexion.

Citations bibliques : **NEG 1979**. Grec/hébreu translittéré + glose. Substrats NA28/BHS.

## Règles d'édition

- **Corrections chirurgicales** : ne toucher que ce qu'exige la demande ; conserver le style,
  la densité académique, la structure, le grec translittéré, les références.
- **`.md` et `.html` doivent rester identiques quant à la prose doctrinale.** Toute correction
  de prose s'applique aux **deux** fichiers (le `.html` porte des entités `&nbsp;` et des
  balises `<i>…</i>` à respecter).
- Les écarts **structurels** `.md` ↔ `.html` sont **voulus** (le `.html` transpose la prose en
  puces, intertitres en gras, chapeau `.lead` + corps). **Ne pas** forcer une parité littérale
  qui casserait le gabarit ; seule la parité du *contenu doctrinal* est exigée.
- Après toute modification du `.md`/`.html`, **régénérer le `.pdf`** correspondant.

## Régénération des PDF

Le script d'origine (ReportLab) n'est pas dans le dépôt. Pipeline de remplacement validé
(pandoc + Chrome headless), produisant un document clair, sérif, paginé :

```bash
# 1) .md -> HTML autonome, feuille de style claire d'impression inlinée
pandoc "<fichier>.md" -f gfm -t html5 --standalone --embed-resources \
  --metadata title="Recherche exégétique : <passage>" -c style.css -o tmp.html
# 2) HTML -> PDF
"chrome.exe" --headless=new --disable-gpu --no-pdf-header-footer \
  --print-to-pdf="<fichier>.pdf" "file:///<chemin>/tmp.html"
```

`style.css` (non commitée) : `@page Letter`, marges ~20 mm, corps `EB Garamond`/Georgia
~11.5 pt justifié, titres accent ambré (`#9a3a12`/`#c2410c`), tableaux encadrés à en-tête
ombré, `print-color-adjust: exact`. Garder un **thème clair** (le thème sombre du site web ne
convient pas à l'impression du dimanche).
