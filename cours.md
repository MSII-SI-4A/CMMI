# CMMI

## Définition

**Processus**

> Suite d'action qui transforme des entrées en sorties en y ajoutant une plus-values. Travaillé sur les processus permet d'améliorer la valeur ajouté

Le meilleur moyen d'y arrivé, c'est de METTRE EN ŒUVRE des "OUTILS" permettant d'AMÉLIORER les processus

**Outils**

"Méthodologique" visant à définir les pratiques|processus à mettre en œuvre

__NORMES__: ISO 9001 (Peu de méthodologie, peu spécialisé, directive formelle certifiant l'organisation)
__MÉTHODE__: Agile, PRINCE (Méthode pure, niveau de détail important, certification de personnes)
__RÉFÉRENTIELS__ de bonne pratique (ITIL, CMMI, COBIT). Construit sur le retour d'expérience "qui marche" et reconnues par la communauté.


Méta-Méthode: moins formelle(quoi faire), mais avec un niveau de détail important, très orienté métier. Certification de personne(ITIL) ou d'organisation(CMMI)

Ex:

- ITIL
- CMMI
- PMI
- Méthode agile
- COBIT
- PRINCE
- ISO 9001


**Ingénierie des systèmes Informatiques**

Cycle de vie du SI:

- Besoins
- Études
- Produit/Développement
- Exploitation
- Maintenance

## CMMI-DEV (Capability Maturity Model Integration)

> Modèle intégré d'aptitude et de maturité pour le développement

Modèle: pas une norme, pas une méthode
maturité: Niveau de maturité des processus mis en œuvre. de 1 à 5 :

1. __Initial__: toutes entreprises au départ
2. __Discipliné__: mise en place de la gestion de projet
3. __Ajusté__: Mise en œuvre des processus technique(Engineering), Organisation Entreprise, Industrialise les process
4. __Gérer quantitativement__:  Mise en place d'outils de statistique
5. __En optimisation__: Pilotage par anticipation basé sur des méthodes statistique

Aptitude d'un processus à atteindre ses objectifs de 0 à 4 :

- 0: __Incomplet__
- 1: __Basique__ :atteinte des résultats
- 2: __Discipliné__ :Moyen, procédure, outils... définis.
- 3: __Ajusté__ : Retour d'experience



Utilisateurs:

- DSI
- SS2I
- Editeur

Appartient au S.E.I : Software Engineering Institute (USA, D.O.D)

Dans les années 70: Beaucoup de bugs dans les systèmes, première version CMM(années 80/90) dans les année 2000 les CMM divergent. Retour à un référentiel central (CMMI) et 3 constellation (DEV, SRV, ACQ)

**Pourquoi**

- Améliorer la performance(V.A) des processus
- Assurer la qualité de service/produit
- Améliorer de la satisfaction client
- Augmenter la productivité/éliminer les coûts
- Offrir une garantie "labellisée" de confiance aux clients
- Demande du marché



## Processus

![Les Niveaux](./niveaux.png)

<table style="width:90%">
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


### Description d'un processus

1. Intention(Définition)
2. liens avec les autres processus
3. Produit d'activité(Paramétres de sorties)
4. Pratiques (Liste de sous-processus)
  - Pratiques "Generique" valable pour plusieurs processus
  - Pratiques "Specifique" lié à un processus
  - Sous-pratique
5. Objectifs
  - Objectifs "Generique" valable pour plusieurs processus
  - Objectifs "Specifique" lié à un processus
6. Exemples
7. Remarques

## Evaluation CMMI

Passage N1 à N2
Exigence: Mettre en oeuvre 7 domaine de processus (PP/PMC,SAM,MA,PPQA,CM,REQM)

Evaluation sur l'entreprise:
- Un budget
- Un évaluateur certifié par S.E.I

## Mise en oeuvre

1. Mode "Projet d'amelioration"
2. Planification



# Quelques reponse aux Questions

Maturité: Niveau de mise en oeuvre des processus
Etude n'est pas une categorie de processus
22 processus
Mise en oeuvre du niveau 1 à Niveau 2 : 18 à 24 mois
Processus de gestion des exigence fait partie de la categorie ingénierie
CMMI est maintenu par SEI
