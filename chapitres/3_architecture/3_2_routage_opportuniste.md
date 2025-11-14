# 3.2 Routage opportuniste

## L'art de saisir les occasions

### L'analogie du réseau neuronal adaptatif

Imaginez un réseau de neurones où les connexions ne sont pas fixes et prédéfinies, mais se forment et se dissolvent dynamiquement selon les besoins et les opportunités. Un neurone A n'envoie pas toujours ses signaux au neurone B spécifique, mais cherche constamment les connexions les plus efficaces disponibles à l'instant présent.

Le routage opportuniste du DNF fonctionne exactement ainsi : au lieu de dépendre de routes fixes et précalculées, il exploite toutes les opportunités de connexion qui se présentent, créant un réseau vivant qui s'adapte en temps réel aux conditions changeantes.

Cette approche révolutionnaire transforme les contraintes (connectivité intermittente, énergie limitée) en opportunités créatives.

## Principes fondamentaux du routage opportuniste

### Au-delà du routage traditionnel

Les réseaux traditionnels utilisent des approches déterministes :
- **Routage statique** : Routes fixes configurées manuellement
- **Routage dynamique** : Calcul de routes optimales basé sur algorithmes
- **Routage par inondation** : Envoi à tous les voisins (coûteux)

Le DNF introduit le **routage opportuniste** :
- **Évaluation continue** : Recherche constante d'opportunités
- **Décisions locales** : Chaque nœud choisit indépendamment
- **Adaptation contextuelle** : S'adapte aux conditions locales

### Les dimensions de l'opportunité

#### 1. Dimension temporelle
- **Disponibilité immédiate** : Connexions actives maintenant
- **Fenêtres temporelles** : Moments où l'énergie est disponible
- **Prévisibilité** : Anticipation des rencontres futures

#### 2. Dimension spatiale
- **Proximité physique** : Distance aux autres nœuds
- **Mobilité relative** : Vitesse et direction des déplacements
- **Couverture géographique** : Zones de forte densité de nœuds

#### 3. Dimension énergétique
- **Niveau de batterie** : Ressources disponibles localement
- **Consommation estimée** : Coût énergétique de la transmission
- **Recharge possible** : Accès à des sources d'énergie

## Algorithmes de routage opportuniste

### L'algorithme Epidemic (Propagation épidémique)

**Principe :** Comme une maladie contagieuse, les messages se propagent à tous les nœuds rencontrés jusqu'à atteindre leur destination.

#### Avantages
- **Simplicité** : Très facile à implémenter
- **Rapidité** : Propagation rapide dans les zones denses
- **Résilience** : Fonctionne même avec peu de connaissances du réseau

#### Inconvénients
- **Coûteux** : Consommation énergétique importante
- **Redondant** : Beaucoup de transmissions inutiles
- **Limité** : Peu adapté aux grands réseaux

#### Optimisations DNF
- **Limite de sauts** : Maximum 7 transmissions par message
- **Filtrage intelligent** : Évite les nœuds déjà infectés
- **Priorisation** : Messages urgents utilisent cette méthode

### L'algorithme PRoPHET (Probabilistic Routing Protocol)

**Principe :** Prédiction des rencontres futures basée sur l'historique des interactions passées.

#### Fonctionnement
- **Historique des rencontres** : Chaque nœud maintient une probabilité de rencontre avec les autres
- **Mise à jour prédictive** : Rencontre = augmentation de la probabilité
- **Transmission sélective** : Envoi aux nœuds les plus susceptibles de rencontrer le destinataire

#### Exemple concret
```
Nœud A cherche à contacter Nœud Z

Historique des probabilités :
- A rencontre B : 0.8 (rencontre fréquente)
- B rencontre C : 0.6 (rencontre régulière)  
- C rencontre Z : 0.3 (rencontre occasionnelle)
- A rencontre Z : 0.1 (rencontre rare)

Route choisie : A → B → C → Z
Probabilité totale : 0.8 × 0.6 × 0.3 = 14.4%
```

#### Avantages
- **Intelligent** : Utilise l'historique pour optimiser
- **Économe** : Réduit les transmissions inutiles
- **Adaptatif** : S'améliore avec le temps

### L'algorithme Spray and Wait

**Principe :** "Vaporiser" des copies du message à quelques relais, puis "attendre" la livraison.

#### Phases
1. **Phase Spray** : Distribution initiale à N relais
2. **Phase Wait** : Attente passive de la livraison

#### Variantes
- **Binary Spray** : Nombre de copies double à chaque étape
- **Source Spray** : Contrôle centralisé du nombre de copies
- **Smart Spray** : Adaptation basée sur la mobilité

#### Exemple
```
Message urgent : 16 copies initiales

Étape 1 : Émetteur donne 8 copies à chaque relais rencontré
Étape 2 : Chaque relais donne 4 copies à son tour
Étape 3 : Chaque sous-relais donne 2 copies
Étape 4 : Livraison directe
```

## Optimisations DNF spécifiques

### L'algorithme Context-Aware Routing (CAR)

Le DNF combine plusieurs approches dans un algorithme propriétaire qui considère le contexte complet :

#### Variables d'entrée
- **Localisation GPS** : Position précise des nœuds
- **Vitesse et direction** : Vecteurs de déplacement
- **Historique social** : Fréquence des rencontres
- **État énergétique** : Niveau de batterie disponible
- **Priorité du message** : Urgence relative

#### Fonction de score composite
```
Score_Route = (Probabilité_Rencontre × 0.4) + 
              (Efficacité_Énergétique × 0.3) + 
              (Fiabilité_Historique × 0.2) + 
              (Priorité_Message × 0.1)
```

#### Décision en temps réel
À chaque rencontre, le nœud évalue :
1. **Dois-je transmettre ?** (Seuil de score > 0.7)
2. **À qui transmettre ?** (Nœud avec le score le plus élevé)
3. **Combien de copies ?** (Basé sur l'urgence)

### Gestion des files d'attente intelligentes

#### Priorisation des messages
- **Urgence maximale** : Accidents, catastrophes (livraison immédiate)
- **Haute priorité** : Santé, sécurité (délai < 1h)
- **Priorité normale** : Communications personnelles (délai < 24h)
- **Basse priorité** : Mises à jour, publicités (délai flexible)

#### Gestion de la congestion
- **Limite de stockage** : Maximum 100 messages par nœud
- **Nettoyage automatique** : Suppression après 7 jours
- **Compression** : Réduction de taille pour économiser l'espace

## Canaux de transmission exploités

### Bluetooth Low Energy (BLE) : Le canal principal

**Caractéristiques :**
- **Portée** : 10-100 mètres (extensible à 1km avec amplificateurs)
- **Consommation** : 0.01-0.5 mA (très économe)
- **Vitesse** : 125 Kbps à 2 Mbps
- **Découverte** : Automatique via beacons

**Usage DNF :**
- **Mesh networking** : Réseau maillé auto-formant
- **Broadcast opportuniste** : Annonce de présence
- **Transmission peer-to-peer** : Échange direct

### WiFi Direct : Pour les connexions rapides

**Avantages :**
- **Vitesse élevée** : Jusqu'à 250 Mbps
- **Portée** : 100-200 mètres
- **Formation de groupes** : Création automatique de réseaux locaux

**Scénarios d'usage :**
- **Zones denses** : Centres urbains, événements
- **Transferts volumineux** : Messages avec pièces jointes
- **Synchronisation** : Mise à jour des annuaires locaux

### NFC et transfert physique

**NFC (Near Field Communication) :**
- **Portée** : Quelques centimètres
- **Usage** : Échange rapide en proximité immédiate
- **Cas d'usage** : Transmission en passant près de quelqu'un

**Transfert physique :**
- **Clés USB** : "Courrier numérique" transportable
- **Cartes SD** : Stockage amovible
- **Applications** : Synchronisation lors de rencontres planifiées

## Gestion de la mobilité

### L'humain comme vecteur de transmission

Une des innovations les plus puissantes du DNF : utiliser les déplacements humains comme système de transport.

#### Modèles de mobilité exploités

1. **Mobilité quotidienne** : Trajets domicile-travail
   - **Prédictible** : Routes régulières
   - **Fréquente** : Plusieurs passages par jour

2. **Mobilité sociale** : Rencontres occasionnelles
   - **Aléatoire** : Cafés, transports en commun
   - **Opportuniste** : Exploitation des rassemblements

3. **Mobilité organisée** : Courriers humains
   - **Planifiée** : Messagers volontaires
   - **Fiable** : Trajets dédiés

#### Exemple de routage via mobilité

```
Marie (Paris) veut contacter Pierre (Marseille)

Route optimale trouvée :
1. Marie → Voiture_Commuter (trajet Paris-Lyon)
2. Voiture_Commuter → Train_TGV (gare de Lyon)
3. Train_TGV → Bus_Régional (gare Marseille)
4. Bus_Régional → Pierre

Temps estimé : 6-8 heures
Énergie consommée : Minimale (stockage passif)
```

## Métriques de performance

### Indicateurs clés du routage opportuniste

#### Métriques de livraison
- **Taux de livraison** : Pourcentage de messages arrivés à destination
- **Délai moyen** : Temps entre envoi et réception
- **Délai médian** : Valeur centrale plus représentative

#### Métriques énergétiques
- **Consommation par message** : Énergie utilisée pour une transmission
- **Efficacité énergétique** : Messages délivrés par unité d'énergie
- **Autonomie réseau** : Durée de fonctionnement sans recharge

#### Métriques de résilience
- **Robustesse aux pannes** : Fonctionnement avec nœuds défaillants
- **Adaptabilité** : Performance dans différents environnements
- **Évolutivité** : Comportement avec plus de nœuds

### Benchmarks réels

**Environnement urbain dense (Paris) :**
- Taux de livraison : 95% en < 2h
- Consommation : 5% de batterie par jour
- Résilience : Fonctionne avec 30% de nœuds actifs

**Zone rurale (Amazonie) :**
- Taux de livraison : 80% en < 24h
- Consommation : 2% de batterie par jour
- Résilience : Routes alternatives via déplacements humains

## Défis et solutions

### Gestion de la scalabilité

**Défi :** Avec millions de nœuds, les calculs deviennent complexes.

**Solutions DNF :**
- **Clustering local** : Décisions prises par groupes de proximité
- **Hiérarchie émergente** : Nœuds "leaders" élus localement
- **Approximation** : Algorithmes probabilistes au lieu d'optimaux

### Gestion de la confidentialité

**Défi :** Les métadonnées de routage peuvent révéler des informations.

**Solutions DNF :**
- **Anonymisation des historiques** : Agrégation statistique
- **Rotation des identités** : Changement régulier des références
- **Chiffrement des métadonnées** : Protection des informations sensibles

## Conclusion : L'opportunité comme stratégie

Le routage opportuniste du DNF représente une rupture paradigmatique : au lieu de combattre les contraintes de la mobilité et de l'énergie limitée, il les embrasse comme des atouts stratégiques.

Comme un navigateur qui utilise les vents et les courants au lieu de lutter contre eux, le DNF utilise la mobilité humaine, les connexions intermittentes, et les ressources limitées pour créer un système de communication plus résilient que tous les réseaux centralisés.

Dans cette approche, chaque rencontre fortuite, chaque déplacement humain, chaque opportunité de connexion devient une occasion de renforcer le tissu communicationnel collectif. Le réseau ne dépend plus d'infrastructures coûteuses, mais de l'intelligence distribuée des interactions humaines quotidiennes.

C'est cette vision opportuniste qui fait du DNF non pas seulement un protocole technique, mais une philosophie de communication adaptée à la réalité complexe et dynamique du monde moderne.
