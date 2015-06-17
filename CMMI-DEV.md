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
 5. Objectifs (2 ... 3)
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

## Processus CMMI-DEV

Les __22__ processus présents dans CMMI-DEV couvrent toutes les activités nécessaires à la fabrication de systèmes.

<table>
	<thead>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; text-align:center; vertical-align:top">
			<p>Acronyme</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; text-align:center; vertical-align:top">
			<p>Domaine de processus</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; text-align:center; vertical-align:top">
			<p>Cat&eacute;gorie et objet des bonnes pratiques propos&eacute;es par le domaine</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; text-align:center; vertical-align:top">
			<p>Mod&egrave;le CMMI et niveau de maturit&eacute; auquel appara&icirc;t le domaine</p>
			</td>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>AM</strong>&nbsp;(<em>Agreement Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion de l&rsquo;accord d&rsquo;acquisition</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: assurer l&rsquo;ex&eacute;cution de l&rsquo;accord par chacune des parties (donneur d&rsquo;ordre et fournisseur).</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>ARD</strong>&nbsp;(<em>Acquisition Requirements Development</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>D&eacute;veloppement des exigences d&rsquo;acquisition</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie d&rsquo;acquisition</strong>&nbsp;: identifier et documenter les exigences client et contractuelles.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>ATM</strong>&nbsp;(<em>Acquisition Technical Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion technique de l&rsquo;acquisition</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie d&rsquo;acquisition</strong>&nbsp;: &Eacute;valuer la solution technique du fournisseur et g&eacute;rer les interfaces entre l&rsquo;acquisition et le syst&egrave;me o&ugrave; elle s&rsquo;int&egrave;gre.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>AVAL</strong>&nbsp;(<em>Acquisition Validation</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Validation de l&rsquo;acquisition</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie d&rsquo;acquisition</strong>&nbsp;: contr&ocirc;ler que l&rsquo;acquisition r&eacute;pond aux besoins op&eacute;rationnels.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>AVER</strong>&nbsp;(<em>Acquisition Verification</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>V&eacute;rification de l&rsquo;acquisition</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie d&rsquo;acquisition</strong>&nbsp;: contr&ocirc;ler que l&rsquo;acquisition est conforme aux exigences.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>CAM</strong>&nbsp;(<em>Capacity and Availability Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion de la capacit&eacute; et disponibilit&eacute;</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: assurer la disponibilit&eacute; et la capacit&eacute; n&eacute;cessaires &agrave; r&eacute;pondre aux exigences du service.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>CAR</strong>&nbsp;(<em>Causal Analysis and Resolution</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Analyse causale et r&eacute;solution</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Support</strong>&nbsp;: analyse des causes de dysfonctionnement pour y porter rem&egrave;de.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 5</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>CM</strong>&nbsp;(<em>Configuration Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion de configuration</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Support</strong>&nbsp;: ma&icirc;trise des &eacute;volutions apport&eacute;es aux &eacute;l&eacute;ments constitutifs de la configuration de r&eacute;f&eacute;rence.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>DAR</strong>&nbsp;(<em>Decision Analysis and Resolution</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Analyse et prise de d&eacute;cision</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Support</strong>&nbsp;: aide &agrave; la prise de d&eacute;cision importante.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>IPM</strong>&nbsp;(<em>Integrated Project Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion de projet int&eacute;gr&eacute;</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: application des processus standard et renforcement de la coordination entre les parties prenantes au projet.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>IRP</strong>&nbsp;(<em>Incident Resolution and Prevention</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Pr&eacute;vention et r&eacute;solution des incidents</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>&Eacute;tablissement et fourniture du service</strong>&nbsp;: pr&eacute;venir et r&eacute;soudre les incidents de service.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>MA</strong>&nbsp;(<em>Measurement and Analysis</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Mesure et analyse</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Support</strong>&nbsp;: fournir des indicateurs r&eacute;pondant aux besoins d&rsquo;information.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>OPD</strong>&nbsp;(<em>Organisational Process Definition</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>D&eacute;finition du processus organisationnel</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management des processus</strong>&nbsp;: documenter les processus standard de l&rsquo;organisation.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>OPF</strong>&nbsp;(<em>Organisational Process Focus</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Focalisation sur le processus organisationnel</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management des processus</strong>&nbsp;: mettre en place une boucle d&rsquo;am&eacute;lioration continue corrigeant les faiblesses constat&eacute;es.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>OPP</strong>&nbsp;(<em>Organisational Process Performance</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Performance du processus organisationnel</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management des processus</strong>&nbsp;: conna&icirc;tre la performance des processus standard de l&rsquo;organisation.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 4</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>OPM</strong>&nbsp;(<em>Organisational Process Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion du processus organisationnel</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management des processus</strong>&nbsp;: aligner en permanence la performance des processus standard de l&rsquo;organisation avec ses besoins business.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 5</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>OT</strong>&nbsp;(<em>Organisational Training</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Formation organisationnelle</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management des processus</strong>&nbsp;: assurer la disponibilit&eacute; des comp&eacute;tences n&eacute;cessaires &agrave; l&rsquo;organisation.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>PI</strong>&nbsp;(<em>Product Integration</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Int&eacute;gration de produit</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie</strong>&nbsp;: assembler et livrer le produit.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>PMC</strong>&nbsp;(<em>Project Monitoring and Control</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Surveillance et contr&ocirc;le de projet</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: suivre l&rsquo;avancement du projet par rapport au plan et corriger les &eacute;carts significatifs.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>PP</strong>&nbsp;(<em>Project Planning</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Planification de projet</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: &eacute;tablir un plan de projet.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>PPQA</strong>&nbsp;(<em>Process and Product Quality Assurance</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Assurance Qualit&eacute; Processus et Produit</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Support</strong>&nbsp;: Identifier et s&rsquo;assurer de la correction des non-conformit&eacute;s processus et produit.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>QPM</strong>&nbsp;(<em>Quantitative Project Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion de Projet quantitative</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: g&eacute;rer le projet en utilisant des techniques quantitatives.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 4</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>RD</strong>&nbsp;(<em>Requirements Development</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>D&eacute;veloppement des exigences</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie</strong>&nbsp;: identifier et documenter les exigences du produit.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>REQM</strong>&nbsp;(<em>Requirements Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion des exigences</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: g&eacute;rer les &eacute;volutions des exigences.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>RSKM</strong>&nbsp;(<em>Risk Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion des risques</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: identifier et r&eacute;duire les risques produit et/ou projet en suivant une strat&eacute;gie organisationnelle.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC, ACQ</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SAM</strong>&nbsp;(<em>Supplier Agreement Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion des accords avec les fournisseurs</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: s&eacute;lectionner les fournisseurs, passer et ex&eacute;cuter l&rsquo;accord.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV, SVC</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SC</strong>&nbsp;(<em>Service Continuity</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Continuit&eacute; de service</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>&Eacute;tablissement et fourniture du service</strong>&nbsp;: documenter et appliquer les plans des activit&eacute;s n&eacute;cessaires &agrave; assurer la continuit&eacute; de service.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SD</strong>&nbsp;(<em>Service Delivery</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Fourniture du service</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>&Eacute;tablissement et fourniture du service</strong>&nbsp;: fournir les services conform&eacute;ment aux accords de service.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SSAD</strong>&nbsp;(<em>Solicitation and Supplier Agreement Development</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>D&eacute;veloppement du dossier de consultation des fournisseurs et de l&rsquo;accord fournisseur</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Management de projet</strong>&nbsp;: pr&eacute;parer un dossier de consultation de fournisseurs, s&eacute;lectionner le ou les fournisseurs et documenter l&rsquo;accord fournisseur.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>ACQ</p>

			<p>Niveau de maturit&eacute; 2</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SSD</strong>&nbsp;(<em>Service System Development</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>D&eacute;veloppement du syst&egrave;me n&eacute;cessaire au service</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>&Eacute;tablissement et fourniture du service</strong>&nbsp;: concevoir et mettre en place un syst&egrave;me pour satisfaire aux besoins des accords de service.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SSM</strong>&nbsp;(<em>Service System Management</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Gestion du syst&egrave;me n&eacute;cessaire au service</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>&Eacute;tablissement et fourniture du service</strong>&nbsp;: mettre en place des services standard align&eacute;s sur les besoins et plans strat&eacute;giques.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>SST</strong>&nbsp;(<em>Service System Transition</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Transition du syst&egrave;me n&eacute;cessaire au service</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>&Eacute;tablissement et fourniture du service</strong>&nbsp;: d&eacute;ployer des &eacute;volutions de composants du syst&egrave;me n&eacute;cessaire au service tout en pr&eacute;servant la fourniture op&eacute;rationnelle du service.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>SVC</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>TS</strong>&nbsp;(<em>Technical Solution</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Solution technique</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie</strong>&nbsp;: Identifier, concevoir et r&eacute;aliser une solution technique en r&eacute;ponse aux exigences.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>VAL</strong>&nbsp;(<em>Validation</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>Validation</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie</strong>&nbsp;: contr&ocirc;ler que le produit r&eacute;pond aux besoins op&eacute;rationnels.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV</p>

			<p>Niveau de maturit&eacute; 3</p>
			</td>
		</tr>
		<tr>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>VER</strong>&nbsp;(<em>V&eacute;rification</em>)</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>V&eacute;rification</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p><strong>Ing&eacute;nierie</strong>&nbsp;: contr&ocirc;ler que le produit est conforme aux exigences.</p>
			</td>
			<td style="border-color:rgb(0, 0, 0) black black; vertical-align:top">
			<p>DEV</p>

			<p>Niveau de maturit&eacute; 3</p>

			<p>&nbsp;</p>
			</td>
		</tr>
	</tbody>
</table>

## Évaluation CMMI

Le passage d'un niveau est réalisé au cours d'une évaluation, cette dernière nécessite :

 - Un budget, 
 - Un évaluateur certifié par le _SEI_,
 - Une équipe d'évaluation,
	 - Employés,
	 - Consultants externes,
 - Un planning,
 - Une méthode d'évaluation (_SCAMPI_),
 - Évaluation sur site,
	 - Entretiens,
	 - Preuves

Il est nécessaire de réunir un certain nombre de conditions, tous les objectifs d'un processus doivent êtres remplis pour que ce dernier soir validé. Il faut que l’ensemble des processus soit validé pour valider le niveau. Pour passer d'un niveau à l'autre il faut :

 - Niveau 2 : Mettre en œuvre 7 domaines,
 - Niveau 3 : Mettre en œuvre 18 domaines,
 - Niveau 4 : Mettre en œuvre 20 domaines,
 - Niveau 5 : Mettre en œuvre 22 domaines.

## Mise en œuvre de CMMI

 1. Passer en mode projet (projet d'amélioration),
 2. Planification (PP),
	 1. Cycle du projet (Cycle en V, Agile...),
		 1. Définition (des processus),
		 2. Déploiement (sur le terrain),
		 3. Bilan,
	 2. Ressources,
		 1. Chef de projet (Interne, expérimenté, connaissance de l'entreprise),
		 2. Équipe projet(Groupe de travail sur les processus),
		 3. Un expert CMMI,
		 4. Sponsor (porteur du projet au niveau de la direction),
	 3. Planning,
 3. Modalités de pilotage,
 	1. Comité de pilotage,
 4. Phase de définition (Par les groupes de travail),
 	1. Définir les processus,
	 	1. Réunions régulières,
	 	2. Formaliser les processus (Activités, ressources...),
	 	3. Vérifier, Valider,
	 	4. Prévoir le déploiement (formation, conduite de changement),
	 	5. Outillage,
 5. Phase de déploiement (faire passer les pratiques sur le terrain),
	 1. Sélectionner les premiers (projets/acteurs) favorables à la démarche,
	 2. Procéder par incrément (ordre des processus),
	 3. Mener la conduite du changement,
		 1. Communication,
		 2. Sensibilisation, formation,
		 3. Implication de la direction,
		 4. Participation collective. 

## Outils

Cette partie liste les outils que l'on ___peut___ mettre en place dans une démarche CMMI. Bien que CMMI ne précise aucuns outils particulier, certains sont indispensables.

### Organisationnel

 - __Bureau de Projets__,
	 - Assistance au démarrage (planning, estimation...),
	 - Support en cours de projet,
	 - Prise en charge du contrôle et de la qualité,
	 - Arbitrage et priorisation entre projets,
 - __Bureau d'ingénierie__,
	 - Exports, garants des savoir faire techniques,
	 - Contrôle des solutions mises en œuvre,
	 - Veille technologique,
	 - Capitalisation des compétences

### Logiciel / progiciel

 - __Gestion du référentiel__ (OPD, OPF),
	 - Comment maintenir et diffuser le référentiel,
	 - Modélisation/cartographie de processus,
	 - Gestion de contenu (GED, CMS),
 - __Gestion de projet__ (PP, PMC, RSKM, MA, PPQA),
	 - MS-Project, SciFormat...
	 - Planification,
	 - Ressources,
	 - Découpage,
	 - Progression,
	 - Tableau de bord,
	 - Gestion des risques,
 - __Ingénierie__ (TS, VER, VAL, REQM),
	 - Outils et méthodes permettant la modélisation (MDA, objet, base de données ...),
	 - Tests,
	 - Gestion des exigences,
 - __Outils de support__:
	 - Gestion des configuration,
	 - Qualité (automatisation des tests),
	 - Décisionnel (Tableaux de bord).

## Bilan

### Avantages

 - Pérénnité certaine,
 - Robuste et éprouvé,
 - Reconnaissance et image forte du label,
 - Contribue à une forte culture d'entreprise,
 - Garantie des résultats,
 - Fonctionne plus facilement dans des environnements stables (DSI, Editeur).

### Inconvénients

 - Diffusion restreinte,
 - Certaine complexité,
 - ROI difficile a démontrer,
 - Démarche longue,
 - Fonctionne difficilement dans des environnements instable (SSII, Start up).