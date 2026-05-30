# Planification : recherche exégétique par section

**Série « La foi qui agit » (Jacques 1 à 5) · 12 semaines**

**2026-05-30** · **AGB** · **EBC**

---

## 1. Objectif

Produire, à l'aide du skill `/sermon-research`, **une recherche exégétique par semaine de prédication** (12 documents), calquée sur la structure de [Recherche Global.md](Recherche Global.md) mais resserrée sur la péricope du dimanche. Chaque recherche doit donner au prédicateur le socle d'étude (contexte, arrière-plan, mots-clés, commentateurs, renvois, thèmes, pistes) avant qu'il ne construise sa structure de prédication.

**Principe directeur :** `Recherche Global.md` reste la recherche d'ensemble (socle de la semaine d'introduction). Elle n'est **pas** à refaire. Les 12 recherches en sont les déclinaisons par unité littéraire, plus profondes sur chaque passage que ne peut l'être un survol de l'épître entière.

## 2. Modèle de référence

`Recherche Global.md` est exactement la sortie de `/sermon-research`. Chaque recherche hebdomadaire reprend ses **7 sections** :

| # | Section | Attendu par passage |
|---|---|---|
| 1 | Contexte du passage | Place de la péricope dans l'argument de l'épître (ce qui précède / suit), pas une réintroduction complète de Jacques. 2-3 paragraphes. |
| 2 | Arrière-plan historique et culturel | Détails que le lecteur moderne manque (anneau d'or, salaire du journalier, onction d'huile…), ciblés sur le passage. 2-3 paragraphes. |
| 3 | Étude des mots-clés | 3 à 5 mots à poids théologique du passage (tableau translit. / sens / champ / S21·NEG79·Darby·LSG·KJF). |
| 4 | Apports des commentateurs | MacArthur, Calvin, Spurgeon, Schreiner, puritains + 1689 LBCF. Question interprétative principale du passage. |
| 5 | Renvois et passages parallèles | 5 à 8 renvois typés : « Parallèle direct », « Lien thématique », « Arrière-plan AT ». |
| 6 | Thèmes théologiques | 3 à 5 thèmes, cadre dogmatique réformé + référence 1689, « Dans le texte » / « Pour votre assemblée ». |
| 7 | Pistes de réflexion | 5 à 7 questions de pression interprétative, propres au passage. |

## 3. Paramètres communs à toutes les recherches

- **Posture :** Baptiste Réformé, lentille MacArthur (TULIP, cessationnisme, Lordship salvation, complémentarisme, prémillénarisme dispensationaliste avec mention honnête de l'alternative covenantale/amillénariste 1689).
- **Langue de sortie :** français canadien, accents et diacritiques **conservés** (aucun texte « déshabillé »). Pas de tirets cadratins dans le contenu.
- **Foundation (`pastor-foundation`) :** `pastor_name` et `church_name` réels (AGB / EBC), jamais d'espaces réservés. Champ `date` à la date de génération.
- **Format de sortie :** un PDF **et** un Markdown frère par recherche, via `python generate-pdf.py sermon-research-temp.json` (installer `reportlab` si absent), puis suppression du JSON temporaire.
- **Convention de nommage :** le générateur nomme d'après le passage, p. ex. `Recherche-Exegetique-Jacques-1-1-12.pdf` / `.md`. Ranger les 12 fichiers dans le dépôt aux côtés des fichiers Global.
- **Anti-patrons à respecter :** aucune structure de prédication, aucun plan en trois points, aucune citation fabriquée, ne pas édulcorer les doctrines de la grâce.

## 4. Fiches de lancement (entrées `/sermon-research` par semaine)

Pour chaque semaine, fournir au skill : **Passage** (requis), **Angle**, **Contexte de série**, **Questions à creuser**. L'angle reprend l'idée maîtresse de [Série Global.md](Série Global.md); les questions croisent fil conducteur, thèmes et pistes de la recherche globale.

### Semaine 1 — La joie au creuset de l'épreuve · Jacques 1.1-12
- **Angle :** Dieu ordonne l'épreuve non pour briser la foi, mais pour la prouver et la mener à maturité.
- **Questions :** distinguer _peirasmos_ épreuve (1.2) vs tentation (prépare la s. 2); prêcher « joie complète » (1.2) sans slogan pieux que les souffrants perceront à jour; _hypomonè_ et persévérance des saints; « couronne de vie » (1.12); le double d'âme (1.6-8).

### Semaine 2 — Le Dieu qui ne change pas · Jacques 1.13-18
- **Angle :** Dieu n'est jamais la source de la tentation; il est la source de tout bien et fait naître par sa parole.
- **Questions :** tenir ensemble « Dieu ne tente personne » (1.13) et sa souveraineté sur l'épreuve (1.2); immutabilité du Père des lumières (1.17); régénération monergique (1.18) comme socle de tous les impératifs à venir.

### Semaine 3 — Auditeurs ou praticiens · Jacques 1.19-27
- **Angle :** une foi qui écoute la Parole sans la pratiquer se trompe elle-même; la religion pure se voit.
- **Questions :** « prompt à écouter, lent à parler » (1.19); le miroir (1.23-25) et le lien direct avec Matthieu 7.21-27; « religion pure » orphelins/veuves (1.27) pour une assemblée à l'aise; énonce le principe de la foi agissante que le ch. 2 développe.

### Semaine 4 — La foi sans partialité · Jacques 2.1-13
- **Angle :** l'acception de personnes selon la richesse contredit la foi au Christ de gloire et viole la loi royale.
- **Questions :** l'anneau d'or et le rang équestre (2.2); la « loi royale » Lévitique 19.18 (2.8); où la partialité se rejoue aujourd'hui; loi de liberté et jugement sans miséricorde (2.12-13).

### Semaine 5 — La foi qui agit · Jacques 2.14-26  ⚠️ *poids doctrinal*
- **Angle :** une foi sans œuvres est morte; la foi qui justifie ne reste jamais seule. Sommet de la série.
- **Questions :** harmoniser Paul et Jacques par les **deux sens de « justifier »** (forensique vs démonstratif); Abraham (Gn 15.6 cité en 2.23) vs l'offrande d'Isaac (Gn 22, en 2.21-22); la foi des démons (2.19); tenir _sola fide_ sans glisser vers la justification par les œuvres ni l'antinomisme; Galates 5.6.
- **Note :** envisager **deux recherches** si scission en deux dimanches — `2.14-19` (la foi morte) et `2.20-26` (Abraham et Rahab).

### Semaine 6 — Le petit membre, le grand feu · Jacques 3.1-12
- **Angle :** la langue, impossible à dompter par le seul effort, révèle l'état réel du cœur.
- **Questions :** « un mal qu'on ne peut maîtriser » (3.8) → ne pas prêcher des conseils pour mieux parler, mais le cœur renouvelé et l'Esprit; jugement plus sévère des maîtres (3.1); « de l'abondance du cœur la bouche parle » (Mt 12.34).

### Semaine 7 — Deux sagesses · Jacques 3.13-18
- **Angle :** la sagesse d'en haut se reconnaît à sa pureté, sa douceur, sa paix, non à l'habileté ni l'ambition.
- **Questions :** _sophia_ comme art de vivre devant Dieu (lien 1.5); opposition sagesse « terrestre, animale, démoniaque » / sagesse « d'en haut »; jalousie et ambition comme racine du mal de la langue (s. 6); charnière vers les conflits du ch. 4.

### Semaine 8 — L'amitié du monde · Jacques 4.1-10  ⚠️ *pastoralement lourd*
- **Angle :** les querelles naissent d'un cœur ami du monde; Dieu résiste à l'orgueilleux, fait grâce à qui s'abaisse.
- **Questions :** « l'amitié du monde est inimitié contre Dieu » (4.4); _dipsychos_, « purifiez vos cœurs, hommes au cœur partagé » (4.8); Proverbes 3.34 cité en 4.6; prêcher l'appel à l'humiliation et à la repentance en encadrant l'avertissement par l'évangile; la grâce qui soutient l'impératif.

### Semaine 9 — Si le Seigneur le veut · Jacques 4.11-17
- **Angle :** juger son frère et présumer de l'avenir relèvent du même orgueil : se mettre à la place de Dieu.
- **Questions :** le jugement du frère (4.11-12) comme péché de la langue; le marchand itinérant qui présume de l'avenir (4.13); la vie « vapeur » et « si le Seigneur le veut » (4.15) comme aveu de dépendance; prépare le contraste avec les riches du ch. 5.

### Semaine 10 — Le cri des moissonneurs · Jacques 5.1-6  ⚠️ *pastoralement lourd*
- **Angle :** la richesse amassée par l'injustice ne sauvera personne au jugement; Dieu entend le cri de l'opprimé.
- **Questions :** le salaire retenu (5.4) à la lumière de Lévitique 19.13 / Deutéronome 24.14-15; « Seigneur des armées » titre d'alliance; le « malheur » prophétique à la manière d'Amos; pour une assemblée riche à l'échelle du monde, déjouer l'esquive « cela vise les ultrariches, pas nous ».

### Semaine 11 — Patience jusqu'à son retour · Jacques 5.7-12  ⚠️ *eschatologie*
- **Angle :** comme le cultivateur attend la pluie, le croyant tient bon car le retour du Seigneur est proche.
- **Questions :** l'imminence, « le juge se tient à la porte » (5.8-9); **mener avec la lecture dispensationaliste prémillénariste de MacArthur, en signalant honnêtement l'alternative covenantale/amillénariste de la 1689**; Job et les prophètes comme exemples de _hypomonè_ (5.10-11); ne pas jurer (5.12); ramène la série à son point de départ tourné vers l'espérance.

### Semaine 12 — La prière qui agit · Jacques 5.13-20  ⚠️ *précision pastorale*
- **Angle :** la communauté de la foi vivante prie en toute saison et va rechercher celui qui s'égare.
- **Questions :** l'onction d'huile et « la prière de la foi » (5.14-15) comme **soin pastoral ordinaire soumis à la volonté de Dieu** — cessationniste mais non sans prière, ni guérison charismatique ni extrême-onction; Élie « homme de la même nature que nous » (5.17-18; 1 Rois 17-18); ramener l'égaré (5.19-20); boucle l'épître.

## 5. Séquence d'exécution

1. **Vérifier l'environnement** : `pastor-foundation` installé (variables AGB/EBC), Python + `reportlab` disponibles.
2. **Lancer les recherches dans l'ordre des semaines** (1 → 12). L'ordre importe : chaque fiche s'appuie sur les précédentes (p. ex. la distinction épreuve/tentation s. 1 → s. 2; le principe de foi agissante s. 3 → ch. 2).
3. Pour chaque semaine : fournir les 4 entrées de la fiche → laisser le skill produire les 7 étapes → générer PDF + `.md` → supprimer le JSON temporaire → noter les noms de fichiers produits.
4. **Semaine 5** : décider d'emblée scission ou non. Si scission, produire deux fiches (`2.14-19`, `2.20-26`).
5. **Semaine d'introduction (optionnelle)** : aucune nouvelle recherche requise — `Recherche Global.md` sert de socle (auteur, destinataires, thèse de l'épître).

## 6. Critères de vérification (par recherche)

- Les 7 sections sont présentes et **scopées sur la péricope**, sans recopier la recherche globale.
- 3 à 5 mots-clés réellement tirés du passage; 5 à 8 renvois typés; 3 à 5 thèmes avec référence 1689 quand applicable; 5 à 7 pistes propres au passage.
- Posture réformée/MacArthur tenue; divergence dispensationaliste/1689 signalée aux passages eschatologiques (s. 11).
- Aucune citation fabriquée, aucune structure de prédication, accents conservés, pas de tirets cadratins.
- PDF + `.md` générés, JSON temporaire supprimé.

## 7. Récapitulatif des livrables

| # | Passage | Fichier attendu |
|---|---|---|
| 1 | Jacques 1.1-12 | `Recherche-Exegetique-Jacques-1-1-12` |
| 2 | Jacques 1.13-18 | `Recherche-Exegetique-Jacques-1-13-18` |
| 3 | Jacques 1.19-27 | `Recherche-Exegetique-Jacques-1-19-27` |
| 4 | Jacques 2.1-13 | `Recherche-Exegetique-Jacques-2-1-13` |
| 5 | Jacques 2.14-26 | `Recherche-Exegetique-Jacques-2-14-26` (ou 2 fichiers si scission) |
| 6 | Jacques 3.1-12 | `Recherche-Exegetique-Jacques-3-1-12` |
| 7 | Jacques 3.13-18 | `Recherche-Exegetique-Jacques-3-13-18` |
| 8 | Jacques 4.1-10 | `Recherche-Exegetique-Jacques-4-1-10` |
| 9 | Jacques 4.11-17 | `Recherche-Exegetique-Jacques-4-11-17` |
| 10 | Jacques 5.1-6 | `Recherche-Exegetique-Jacques-5-1-6` |
| 11 | Jacques 5.7-12 | `Recherche-Exegetique-Jacques-5-7-12` |
| 12 | Jacques 5.13-20 | `Recherche-Exegetique-Jacques-5-13-20` |
