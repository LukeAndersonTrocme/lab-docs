# Données de recherche sensibles : guide d'intégration pour étudiants

Tous les laboratoires de recherche ne travaillent pas avec des données sensibles. Un projet portant sur les populations d'insectes ou la couverture forestière repose sur des données qui comportent peu de risques pour la vie privée. Notre laboratoire est différent. Parce que nous travaillons avec des données généalogiques humaines — et parfois avec des dossiers de santé et de l'ADN — les individus et les familles représentés dans nos bases de données ont un intérêt réel à la façon dont leurs informations sont traitées. Bon nombre de ces personnes sont vivantes; d'autres ont des descendants vivants. Les cadres légaux auxquels nous sommes soumis existent pour de bonnes raisons, et ce guide aussi. Comprendre comment travailler de façon responsable avec des données sensibles n'est pas seulement une obligation réglementaire : c'est une forme de respect envers les personnes qui se trouvent derrière les dossiers.

> **Règle fondamentale :** Les données du projet sont confidentielles et doivent demeurer en tout temps sur les grappes de calcul de l'Alliance de recherche numérique du Canada (Calcul Canada). Les statistiques sommaires agrégées peuvent être exportées. En cas de doute, consultez le chercheur principal avant d'agir.

---

## Avant de commencer : liste de vérification

*Compléter les étapes suivantes **avant** d'accéder aux données du projet.*

- [ ] Lire le [guide de classification des niveaux de confidentialité de l'UdeM (PDF)](https://vie-privee.umontreal.ca/fileadmin2/vie-privee/documents/exemples-rp.pdf). Porter une attention particulière aux exemples de niveau 4 (données de santé, ADN) pour comprendre où se situent nos données sur le spectre de la sensibilité.
- [ ] Compléter la formation en ligne **EPTC 2 : CORE-2022** (~4 h) sur [tcps2core.ca](https://tcps2core.ca/welcome). Le certificat obtenu vaut la peine d'être conservé — c'est un titre reconnu qui vous suivra au-delà de ce laboratoire et qui renforce toute demande future auprès d'un comité d'éthique.

---

## Principes directeurs

Ce ne sont pas des règles bureaucratiques. Ce sont des habitudes qui valent la peine d'être cultivées pour tout futur travail avec des données humaines.

**L'ADN et les dossiers de santé comptent parmi les données les plus sensibles qu'un chercheur puisse manipuler.** L'UdeM les classe au niveau 4 sur 5.

**La structure de la généalogie est elle-même sensible.** Même sans noms, savoir qui est apparenté à qui — ou quelles familles portent certains traits génétiques — peut exposer des informations profondément privées sur des personnes réelles et leurs descendants vivants. Un arbre généalogique n'est pas une structure de données neutre.

**Avant de transférer quoi que ce soit hors de la grappe, faites une pause.** Demandez-vous : « Suis-je explicitement autorisé(e) à transférer ces données? » Pas « je pense que ça devrait aller ». Si vous n'en êtes pas certain(e), demandez d'abord au chercheur principal. Le coût de poser la question est nul. Le coût d'une brèche ne l'est pas.

**En cas de doute, ne faites rien et demandez.** Cela s'applique aux transferts de données, au partage de résultats, à l'utilisation de nouveaux outils, ou à toute autre situation où des données risquent de quitter leur environnement autorisé. La prudence est toujours la bonne valeur par défaut.

---

## 1. Cadre légal et réglementaire

### Loi 25 (*Loi modernisant des dispositions législatives en matière de protection des renseignements personnels*)

En vigueur depuis septembre 2023, la Loi 25 renforce considérablement les obligations en matière de protection de la vie privée pour tous les organismes québécois, incluant les universités. Points clés pour la recherche :

- **Les évaluations des facteurs relatifs à la vie privée (ÉFVP)** sont légalement requises pour les projets impliquant la collecte, la création ou la réutilisation de renseignements personnels. Comme ce projet réutilise des données existantes plutôt que d'en collecter de nouvelles, une ÉFVP n'est peut-être pas obligatoire — mais le chercheur principal doit le confirmer. Pour obtenir des conseils, contacter le bureau de la protection de la vie privée de l'UdeM : [vie-privee@umontreal.ca](mailto:vie-privee@umontreal.ca).
- L'accès aux renseignements personnels doit être limité aux seules personnes autorisées.
- Les violations de données doivent être signalées à la Commission d'accès à l'information (CAI) et aux personnes concernées.

### EPTC 2 — Énoncé de politique des trois Conseils : Éthique de la recherche avec des êtres humains

Cadre national canadien régissant la recherche éthique impliquant des participants humains. Toutes les universités qui reçoivent du financement des trois organismes fédéraux (CRSNG, CRSH, IRSC) y sont soumises.

Le tutoriel en ligne **CORE-2022** sur [tcps2core.ca](https://tcps2core.ca/welcome) est gratuit, à votre propre rythme (~4 h), et couvre la vie privée, le consentement, la sécurité des données et la recherche impliquant des communautés autochtones. Le certificat de réussite est généralement requis pour les demandes soumises aux comités d'éthique de la recherche (CÉR) ; conservez-en une copie.

### Politiques institutionnelles de l'UdeM

Les politiques suivantes régissent le traitement de l'information. Le [guide de protection des données de recherche](https://vie-privee.umontreal.ca/proteger-les-donnees-de-recherche/) renvoie au texte intégral de chacune.

---

## 2. À propos des données du labo

### Type de données

Ce labo repose sur des données généalogiques compilées par le groupe de généalogie Balsac. Les données peuvent inclure des identifiants, des dates de naissance/décès/mariage, des liens de parenté, des informations géographiques, ainsi que du matériel issu de recensements historiques, d'actes de l'état civil et de dossiers notariaux. Certains enregistrements peuvent être liés à des données de santé ou à des données d'ADN.

Même lorsqu'elles proviennent de sources historiques, les données généalogiques peuvent contenir des **renseignements personnels sur des personnes vivantes ou leurs descendants récents** et doivent être traitées comme sensibles.

### Ce qui peut être partagé

| Type de données | Permis? |
|-----------------|---------|
| Statistiques sommaires / agrégées (effectifs, taux, distributions) | ✓ Oui — peuvent être exportées |
| Résultats anonymisés où la réidentification n'est pas raisonnablement possible | ✓ Avec l'approbation du chercheur principal |
| La structure des relations généalogiques (arbres, réseaux familiaux) | ✗ Sensible — doit rester sur la grappe |
| Données au niveau individuel, même sous forme modifiée | ✗ Doit rester sur la grappe |
| Fichiers de données brutes | ✗ Doit rester sur la grappe |

En cas de doute sur l'exportabilité d'un résultat, demandez au chercheur principal.

---

## 3. Stockage des données

### Principal : grappes de calcul de l'Alliance (Calcul Canada)

Les données du projet résident sur les grappes de l'Alliance. Elles ne doivent **pas** être transférées vers :

- Des ordinateurs portables ou des postes personnels
- Des services infonuagiques personnels (Google Drive, Dropbox, iCloud, OneDrive, etc.)
- Des clés USB ou des disques durs externes
- Des pièces jointes de courriel

Toute analyse doit être effectuée directement sur la grappe via SSH ou à travers des interfaces distantes autorisées. Ne stockez jamais de données localement, même temporairement.

### Secondaire : le poste de travail du laboratoire (le « TrashMac »)

Le laboratoire dispose d'un poste de travail dédié à l'UdeM — un ordinateur de bureau chiffré, muni d'un dispositif antivol. Dans des cas spécifiques, certaines données peuvent y être stockées ou traitées. **Cela nécessite une approbation explicite du chercheur principal à l'avance.** Ne copiez pas de données sur le TrashMac sans avoir préalablement confirmé avec le chercheur principal.

---

## 4. Poste de travail et accès

Si vous travaillez depuis un **ordinateur portable personnel**, aucune donnée sensible ne doit jamais y être stockée. Tout accès aux données du projet doit passer par la grappe de l'Alliance via SSH, JupyterHub ou une autre interface distante autorisée. Votre ordinateur est un terminal — pas un espace de stockage.

Ne partagez vos identifiants de connexion à la grappe avec personne.

---

## 5. Outils d'intelligence artificielle

Ne soumettez aucune donnée sensible du projet à des outils d'IA — y compris, sans s'y limiter, Claude, ChatGPT, GitHub Copilot, ou tout autre assistant qui traite ou transmet des données à l'externe.

Cela inclut :

- Coller des enregistrements de données dans une interface de clavardage
- Téléverser des fichiers de données vers un service d'IA
- Utiliser des assistants de programmation par IA susceptibles d'envoyer du contexte de code contenant des données intégrées à des serveurs externes

Le code et les statistiques sommaires sans données intégrées sont généralement acceptables. Si vous n'êtes pas sûr(e) qu'un outil ou un cas d'utilisation précis est permis, demandez d'abord au chercheur principal.

---

## 6. Signalement d'un problème

Si vous soupçonnez une violation de données, un accès non autorisé ou une divulgation accidentelle — ou si vous n'êtes simplement pas certain(e) qu'une action planifiée est permise :

1. **Arrêtez immédiatement l'action.**
2. Avisez le chercheur principal dès que possible.
3. Le chercheur principal transmettra l'information au bureau de la vie privée de l'UdeM si nécessaire : [vie-privee@umontreal.ca](mailto:vie-privee@umontreal.ca)

Ne tentez pas d'enquêter sur une violation ou de la corriger par vous-même.

---

## 7. Ressources clés

| Ressource | Lien |
|-----------|------|
| Formation en éthique EPTC 2 : CORE-2022 | [tcps2core.ca](https://tcps2core.ca/welcome) |
| Guide de classification de la confidentialité de l'UdeM (PDF) | [vie-privee.umontreal.ca](https://vie-privee.umontreal.ca/fileadmin2/vie-privee/documents/exemples-rp.pdf) |
| Guide de protection des données de recherche de l'UdeM | [vie-privee.umontreal.ca](https://vie-privee.umontreal.ca/proteger-les-donnees-de-recherche/) |
| Boîte à outils de l'Alliance — Partie 1 : Glossaire | [Zenodo](https://zenodo.org/records/4088946) |
| Boîte à outils de l'Alliance — Partie 2 : Matrice de risques | [Zenodo](https://zenodo.org/records/4088954) |
| Ressources de formation de l'Alliance (GDR) | [alliancecan.ca](https://www.alliancecan.ca/en/our-services/research-data-management/learning-resources/training-resources) |
| Bureau de la protection de la vie privée de l'UdeM | [vie-privee@umontreal.ca](mailto:vie-privee@umontreal.ca) |

---

*Dernière mise à jour : 2026-03-13. Document maintenu par le chercheur principal. Questions? Contactez le chercheur principal ou le bureau de la vie privée de l'UdeM.*
