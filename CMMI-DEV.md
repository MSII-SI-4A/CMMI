# CMMI

## Définitions

__CMMI__ : _Capability Maturity Model Integration_ (_Modèle Intégré d'Aptitude et de maturité pour le Développement_) appartient au _SEI_,  
__SEI__ : _Software Engeneering Institute_ anciennement nommé DOD (Department Of Defence),  
__CMMI-DEV__ : Référentiel de bonne pratiques destiné a l'étude et au développement de systèmes. Il est utilisé par la DSI, les SSII, les éditeurs ...   
__Processus__ : Transformation d'un flux d'entré en un flux de sortie en y appliquant un traitement. Ce traitement ajoute de la __valeur ajouté__ et a des objectifs et peut être contrôlé.

__Maturity__ : Niveau de maturité des pratiques et de processus mis en œuvre dans l'entreprise; elle se mesure en 5 niveaux : 

 1. __Initiale__ : Niveau de base, pas de niveau zéro,
 2. __Discipliné__ : Mise en place de la gestion de projet,
 3. __Ajusté__ : Mise en œuvre des processus techniques/engeneering et organisation entreprise,
 4. __Gérer quantitativement__ : Mise en place d'outils statistiques,
 5. __En optimisation__ : Pilotage par anticipation basé sur des méthodes statistiques.

__Capability__ : Aptitude d'un processus a atteindre ses objectifs. Il en existe 4 niveaux : 

 0 - __Incomplet__ : Résultat non atteins,  
 1 - __Basique__ : Résultats atteins,  
 2 - __Discipliné__ : Résultats atteins, procédure, outils... définis,  
 3 - __Ajusté__ : Résultats atteins, procédure, outils... définis, retours d'expérience -> industrialisation.

Le meilleur moyen d'améliorer les processus (production de V.A.) est de mettre en œuvre des outils méthodologique visant à définir les pratiques à mettre en œuvre permettant d'améliorer les processus. Ex : (ITIL, Méthodes agile, COBIT, PRINCE, PMI, CMMI, ISO)

 - __Normes__ : Peu méthodologique, directives formelles, certification d'organisations (ISO 9001),
 - __Méthodes__ : Méthode pure, niveau de détail import, certification des personnes (Agile, PRINCE),
 - __Référentiels__ : Bonnes pratiques, retours d'expériences qui fonctionne, Méta-Méthode, moins de directives formelles, niveau de détail important, orienté métier, certification des personnes et d'organisations (ITIL, CMMI).

__Cycle de vie du S.I.__ :
 
 1. Récupération des besoins,
 2. Étude (faisabilité, contraintes ...),
 3. Développement,
	1. Exploitation,
	2. Maintenance.

Les différents outils se placent comme suit : 

 - ITIL : 3.1, 3.2
 - ISO 9001 : 2, 3, 3.2
 - CMMI : 2, 3

## Historique

Suite au constat au cours des années 70 que les systèmes comptent beaucoup de bugs, le département de la défense américaine met en place le SEI dans les universités d'état. Au cours des années 80 et 90 une registre de bonne pratiques pour tous les systèmes nommé _CMM_ est publié. Suite a des adaptations nombreuses pour tous les domaines, il est refondu en 2000 pour donner naissance a _CMMI_. Ce dernier se compose d'un référentiel central et de trois constellation qui en dérivent : 

 - DEV : Développement de systèmes
 - ACQ : Acquisition de systèmes (maître d’œuvre)
 - SRV : Service, aspect support, maintenance et exploitation

## Pourquoi ?

Pourquoi choisir de mettre en œuvre un référentiel de bonnes pratiques ?

 - Améliorer la performance des processus,
 - Assurer la qualité de service et des produits,
 - Améliorer la satisfaction client,
 - Optimiser les coûts,
 - Offrir une garantie labellisée,
 - Demande du marché.

## Processus CMMI-DEV

Les __22__ processus présents dans CMMI-DEV couvrent toutes les activités nécessaires à la fabrication de systèmes.

### Niveau 2 (7 processus)

#### Planification (PP)

#### Suivi de projet (PMC)

Project Management and Control

#### Gestion de la sous-traitance (SAM)

Suplier Agreement Management

#### Gestion des exigences (REQM)

#### Gestion de la qualité (PPQA)

#### Mesure et analyse de mesure

#### Gestion de configuration (CA)

### Niveau 3 (11 processus)

#### Conception et développement (TS)

Technical Solution

#### Intégration (PI)

#### Développement des exigences (RD)

Requirement Developpement

#### Prise de décision (DAR)

#### Vérification - Confrontation aux exigences (VAR)

#### Validation - Confrontation aux besoins (VAL)

#### Définition des processus (OPD)

Organization Process Definition

#### Amélioration des processus (OPF)

Organization Process Focus

#### Formation (OT)

Organization trainning

#### Gestion des risques (RSKM)

Risk Management

#### Gestion de projet intégré (IPM)

Integrated Project Management

### Niveau 4 (2 processus)

#### Gestion quantitative des projets (QPM)

#### Gestion de la performance des processus (OPP)

Organization Process Performance

### Niveau 5 (2 processus)

#### Analyse causale (CAR)

#### Amélioration de la performance des processus (OPM)

Organization Process Management

## Architecture CMMI

### Exemple : Planification de projet

__Activités__ :

- Déterminer les tâches : Décomposer le projet (_WBS_ : Work Breakdown Structure)
- Identifier les ressources : Monter une équipe
- Faire une estimation (de charge)
- Faire un planning (date de début, fin, jalons)
- Faire le budget
- Identifier la logistique (moyens, locaux ...)
- Modalités de pilotage
- Planifier les formations

### Architecture standard 

Les processus sont représentés de la manière suivante dans CMMI : 

 1. Intention (Définition)
 5. Objectifs
	 1. Objectifs Génériques
	 2. Objectifs Spécifiques
 3. Produits d'activité (Paramètres de sortie)
 4. Références entre domaine de processus (Liens avec d'autres processus)
 5. Pratiques (Liste des activités)
	 1. Pratiques génériques (Applicables à tous les processus)
	 2. Pratiques spécifiques (Applicable au processus)
	 3. Sous pratiques (Liste des activités pour une activité mère)
 6. Exemples
 7. Remarques

````csharp
namespace fr.eni.msiisi.4a.model.cmmi{

	interface Target{}
	class GenericTarget : Target{}
	class SpecificTarget : Target{}
	
	interface Practice{}
	interface HightLevelPractice : Practice { List<Practice> SubPractices {get;set;}; };
	
	class GenericPractice : Practice{}
	class SpecificPractice : Practice{}
	class HightLevelPractice : HightLevelPractice{}
	
	class Result{
		String Description;
		String Name;
	}
	
	class Process{
		String Intention;
		List<Target> Targets;
		List<Result> ActivityProducts;
		List<HightLevelPractice> Practices;
		List<Process> References;
		List<String> Samples;
		List<String> Remarks;
	}

}
````

