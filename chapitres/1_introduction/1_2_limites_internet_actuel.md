# 1.2 Les limites d'Internet actuel

## L'architecture centrale comme talon d'Achille

### L'analogie du système nerveux centralisé

Imaginez Internet comme un système nerveux géant où toutes les décisions passent par un cerveau central unique. Dans le corps humain, cette centralisation serait catastrophique : une lésion cérébrale paralyserait immédiatement tout l'organisme. Pourtant, c'est exactement le modèle qu'Internet a adopté.

Les serveurs DNS racine, ces 13 machines stratégiques situées principalement aux États-Unis, constituent le "cerveau" d'Internet. Elles traduisent les noms de domaine familiers (google.com, amazon.fr) en adresses IP compréhensibles par les machines. Si ces serveurs venaient à être compromis ou défaillants, l'ensemble du réseau mondial serait désorienté.

### Les points de défaillance critiques

#### 1. Les câbles sous-marins : artères vitales

Plus de 99% du trafic Internet international transite par des câbles sous-marins reliant les continents. Ces câbles, souvent plus fins qu'un doigt humain, sont vulnérables à :

- **Les ruptures accidentelles** : Chaluts de pêche, ancres de navire, glissements de terrain
- **Les sabotages intentionnels** : Coupes délibérées pour des raisons géopolitiques
- **Les catastrophes naturelles** : Tremblements de terre, éruptions volcaniques

En 2023, des câbles sous-marins ont été sectionnés près de la Syrie, isolant temporairement plusieurs pays du Moyen-Orient. En 2022, un câble endommagé au large de Taïwan a perturbé les communications dans toute l'Asie du Sud-Est.

#### 2. Les data centers : forteresses énergivores

Les centres de données modernes sont des cathédrales technologiques :
- **Consommation énergétique massive** : Un data center Google consomme autant d'électricité qu'une ville de 50 000 habitants
- **Dépendance aux réseaux électriques** : Sans électricité stable, ils deviennent inertes
- **Concentration géographique** : La plupart sont situés dans des zones tempérées avec accès à l'eau pour le refroidissement

Lors des pannes de courant massives, comme celles survenues en Inde en 2022 (affectant 620 millions de personnes), les data centers deviennent les premiers à tomber, emportant avec eux les services cloud essentiels.

#### 3. Les infrastructures de télécommunication : château de cartes

Les tours de téléphonie mobile et les antennes satellite reposent sur une cascade de dépendances :
- **Alimentation électrique** : Batteries de secours limitées à quelques heures
- **Connexions terrestres** : Câbles reliant les tours aux centres de contrôle
- **Maintenance spécialisée** : Techniciens formés et pièces de rechange disponibles

## Les vulnérabilités opérationnelles

### La fragilité des chaînes d'approvisionnement

Internet moderne dépend d'une chaîne logistique globale complexe :
- **Semi-conducteurs** : Produits principalement à Taïwan (TSMC)
- **Câbles de fibre optique** : Matériaux rares et processus de fabrication spécialisés
- **Équipements réseau** : Concentrés dans quelques fabricants mondiaux

Une perturbation dans n'importe quel maillon (conflits commerciaux, pandémies, guerres) peut créer des pénuries affectant des millions d'appareils.

### Les limites de la mobilité

Dans les zones reculées ou en mouvement, Internet traditionnel montre ses faiblesses :
- **Couverture satellite** : Coûteuse et limitée en débit
- **Réseaux mobiles** : Dépendants des infrastructures terrestres
- **Connexions par satellite** : Vulnérables aux conditions météorologiques et aux interférences

Les nomades numériques, les expéditions scientifiques, ou les populations vivant dans des zones isolées se retrouvent souvent déconnectés, non par choix, mais par contrainte technologique.

## Les aspects socio-économiques

### L'inégalité numérique amplifiée

Internet actuel creuse le fossé entre les régions développées et isolées :
- **Zones urbaines denses** : Connexions haut débit omniprésentes
- **Régions rurales** : Coûts prohibitifs pour déployer des infrastructures
- **Pays en développement** : Dépendance aux investissements étrangers pour les câbles

Cette inégalité crée une "fracture numérique" où l'accès à l'information et aux opportunités économiques dépend de la géographie physique.

### La dépendance aux intermédiaires

Les grands acteurs technologiques contrôlent des pans entiers d'Internet :
- **Services DNS** : Google Public DNS, Cloudflare
- **Infrastructure cloud** : AWS, Azure, Google Cloud
- **Réseaux sociaux** : Facebook, Twitter, TikTok

Cette concentration crée des risques :
- **Censure politique** : Possibilité de blocage sélectif
- **Surveillance généralisée** : Collecte massive de données personnelles
- **Monopoles économiques** : Prix fixés par quelques acteurs

## Les défis environnementaux

### L'empreinte carbone massive

Internet représente environ 3-4% des émissions mondiales de CO2 :
- **Data centers** : Consommation électrique équivalente à l'aviation civile
- **Réseaux de transmission** : Énergie pour amplifier les signaux sur les câbles
- **Appareils terminaux** : Fabrication et utilisation énergétique

Dans un contexte de changement climatique, cette empreinte carbone devient problématique, surtout lorsque les infrastructures sont détruites par des catastrophes qu'elles contribuent à aggraver.

### La gestion des déchets électroniques

Le renouvellement rapide des équipements crée des montagnes de déchets :
- **Téléphones obsolètes** : Millions d'appareils jetés chaque année
- **Équipements réseau** : Matériel remplacé tous les 3-5 ans
- **Data centers** : Serveurs devenus inutiles après quelques années

Ces déchets contiennent des matériaux précieux mais aussi des substances toxiques, créant des problèmes environnementaux locaux et globaux.

## Les limites de sécurité et de confidentialité

### La surveillance de masse

L'architecture centralisée facilite la surveillance :
- **Points de contrôle uniques** : Tous les paquets passent par des routeurs contrôlables
- **Logs centralisés** : Traçabilité complète des communications
- **Attaques ciblées** : Compromission d'un nœud affecte des millions d'utilisateurs

### Les attaques distribuées

Les DDoS et autres cyberattaques exploitent la centralisation :
- **Amplification des effets** : Une attaque sur un point central paralyse tout
- **Cascades de défaillance** : Une vulnérabilité se propage rapidement
- **Rançongiciel** : Prise d'otage des infrastructures critiques

## Vers une nouvelle approche

Face à ces limites structurelles, il devient évident qu'Internet traditionnel, malgré ses succès extraordinaires, n'est plus adapté aux défis du XXIe siècle. Comme un bâtiment magnifique mais construit sur des fondations instables, il risque de s'effondrer sous le poids de ses propres succès.

Le DNF propose une alternative : non pas remplacer Internet, mais l'étendre avec une approche résiliente qui transforme les contraintes en opportunités. Au lieu de dépendre d'infrastructures coûteuses et vulnérables, il utilise les ressources déjà présentes dans nos poches : nos téléphones mobiles, devenus les véritables citoyens du réseau distribué.
