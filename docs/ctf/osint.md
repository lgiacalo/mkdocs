# Osint

Qui dit social engineering, dit obligatoirement recherche d’informations via de multiples sources. De cette constatation, l’utilisation de techniques d’OSINT est un élément indispensable. OSINT signifie Open Source Intelligence. Cet anglicisme regroupe un ensemble de techniques et d’outils qui permettent de collecter des renseignements sur une personne, une entreprise, une situation économique dans un pays.

Des recherches et un regroupement d’informations proposés par Internet. Du Renseignement de Source ouverte : réseaux sociaux, moteurs de recherche, sites web... L’OSINT s’intègre dans trois autres grands points à prendre en compte :

- Open Source Data (OSD) : les données récupérables à partir de sources dites primaires : une lettre trouvée dans une poubelle, une photographie sur un réseau social, un message sur un répondeur... Des informations qu’il faudra affiner avec les autres points.

- Open Source Information (OSIF) : on pourra baptiser l’OSIF comme étant une "revue de presse" : le regroupement d’informations tirées de journaux, de livres, de conférences, de rapports extraits d’universités, de conférences de presse, etc.

- Validated OSINT : connue sous le nom d’OSINT-V, cette étape classifie les informations collectées comme étant très sûres. Parmi ces documents OSINT-V, les notes internes, réalisées par exemple par les services de renseignement, les ambassades, que reçoivent les chefs d’états. On parlera dans ce cas d’informations à haut degré de sécurité.


## WM - TL-OSINT - une machine virtuelle pour l’OSINT

Pour ceux qui ne veulent pas installer les outils un à un, l’équipe de Trace Labs a implémenté une VM OSINT qui rassemble les outils OSINT les plus efficaces et de nombreux scripts personnalisés. La VM est basée sur une version modifiée de la célèbre distribution Kali-Linux. On peut la télécharger ici : https://www.tracelabs.org/initiatives/osint-vm

- [Trace Labs OSINT VM - Introduction and Installation](https://www.youtube.com/watch?v=jjK0nvmOeUA)
- [Trace Labs OSINT VM - Live Demo with Q&A Webinar](https://www.youtube.com/watch?v=yZdOb-NSiAw)

## Outils

Il existe des centaines de logiciels dédiés à l’OSINT. Ils permettent de regrouper des informations, de collecter de la donnée sur une personne. Attention cependant, le meilleur des logiciels restera votre cerveau. Voici sept de ces outils. Votre curiosité et vos entraînements feront le reste.

### [Google](https://www.google.com)

Qu’on le veuille ou non, Google est l’outil indispensable à placer dans votre boîte à outils OSINT. Il permet, à partir de commandes baptisées dork, d’extraire de l’information pouvant être très ciblée. Voici un exemple. Dans la barre de recherche du moteur de recherche américain, tapez la commande INURL:.txt @orange.fr. Nous prenons ici l’exemple @orange.fr, mais vous pouvez proposer à la recherche toutes les informations de votre choix. Vous pouvez y placer, par exemple, le nom de votre entreprise. Nous allons vous traduire cette commande. INURL demande à Google de chercher dans toutes les URL qu’il possède en mémoire des adresses web avec un fichier texte .TXT. La commande globale vous indiquera tous les sites proposant des fichiers textes comportant des adresses @orange.fr.


### [Shodan](https://www.shodan.io)

Shodan propose les résultats les plus poussés pour les spécialistes de la sécurité informatique. Soyons honnêtes, pas seulement eux. De nombreux pirates exploitent cet outil extrêmement puissant pour rechercher, par exemple, des informations relatives aux objets connectés : ordinateurs, serveurs, NAS, feux de signalisation, caméras de vidéosurveillance...

https://www.shodan.io

### [Creepy](https://www.geocreepy.com/)

Cet outil porte bien son nom. Ce "terrifiant" programme permet de géolocaliser une personne, un lieu, via les informations de géolocalisation en source ouverte que peuvent fournir les réseaux sociaux, les plateformes de sauvegarde de documents (images, etc.). Creepy tourne sous Windows et Linux.

https://www.geocreepy.com/

### [Spyse](https://spyse.com/)

Petit frère de Shodan, Spyse offre un nombre d’informations concernant une "cible" loin d’être négligeable. Vous commencez avec un nom de domaine et vous pouvez pousser votre enquête en vérifiant ensuite vulnérabilités, adresses IP, DNS, noms de domaines sur la même adresse IP, etc.

https://spyse.com/

### [Epieos](https://tools.epieos.com)

L’outil proposé par Epies va vous permettre d’extraire toutes les informations cachées derrière une adresse électronique. Dans la barre baptisée Enter the target email address, vous entrez le courriel cible. Epieos va ensuite vous fournir, très rapidement l’identité cachée derrière ce courriel, sa date de création, son utilisation possible dans Google, l’ID Google, photos et calendrier accolés à cette adresse, les réseaux sociaux.

https://tools.epieos.com

### [OSINT Framework](https://osintframework.com/)

Comme son nom l’indique, OSINT Framework propose un ensemble d’outils pour lancer des recherches. Par exemple, vous cherchez une identité, il vous suffit de cliquer sur Username, puis OSINT Framework vous propose les logiciels et les sites qui vous permettront de remonter à votre source. Ce site web offre des dizaines de possibilités, par secteur de recherche : adresses e-mail, noms de domaine, archives, etc.

- https://osintframework.com/
- [GihtHub](https://github.com/lockfale/OSINT-Framework?tab=readme-ov-file) : https://github.com/lockfale/OSINT-Framework?tab=readme-ov-file

### [Osint Collection](https://start.me/p/b5Aow7/asint_collection)

Dans la même lignée d’OSINT Framework, OSINT Collection regroupe des centaines d’outils dédiés à la recherche d’informations via des sources ouvertes. Classée par qualité (médias sociaux, moteurs de recherche spécialisés), cette collection permet de travailler sur des outils atypiques, comme des moteurs de recherche russe ou chinois tels que VK ou encore Qzone et Renren.

https://start.me/p/b5Aow7/asint_collection

### GIJN - [gijn.org/fr](gijn.org/fr)

- [Guide pour enquêter en ligne](https://gijn.org/fr/ressource/guide-pour-enqueter-en-ligne/)
- [Research and investigation links - Auteur de l'article](https://researchclinic.net/)