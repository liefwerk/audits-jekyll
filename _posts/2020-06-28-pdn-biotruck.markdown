---
layout: post
title:  "Prises de notes - biotruck"
date:   2020-06-18 00:04:49 -0300
categories: jekyll update
---

## Résumé de l'activité

L'activité de GMLB est de faire les marchés locaux et de livrer à domicile des fruits et légumes de saisons et locaux.
Bio-truck se concentrera principalement sur la livraison à domicile.

Partage des zones géographiques entre les deux plateformes.
Structure identique mais différence visuelle.

### Objectifs de la nouvelle plateforme

- Faciliter le suivi des commandes
- Créer une base de donnée de produits réutilisable

### Challenges identifiés

Ordonner les challenges par ordre d'importance.

- Convaincre les utilisateurs existants d'utiliser la nouvelle plateforme
  - Comprendre leurs habitudes
- Faciliter la recherche de produits
- Trouver de nouveaux utilisateurs
  - Stratégie SEO locale
  - Identifier les concurrents
- Ajouter tous les produits
  - Chercher si possibilité d'ajouter via un fichier (Excel ou JSON)
  - [Importer/exporter via CSV](https://docs.woocommerce.com/document/product-csv-importer-exporter/)
  - Enseigner comment ajouter produits facilement
  - Mise en ligne des images avec descriptions (outil ?)
- Fonctionnalités à ajouter
  - Empêcher les commandes de moins de 20€
  - Spécifier le minimum de commande dans le panier
  - Vérifier si on peut faire des groupes de produits pour créer les paniers
- Cloner le ftp

## whatweb - Analyse des technologies utilisées par le site internet

### <http://gmlb-et-ses-biobons.com/>

- Apache
- Country [GERMANY]
- HTML5
- IP [92.222.139.156]
- WooCommerce [4.2.0]
- WordPress [5.4.2]
- PHP [7.2]

## Page SpeedInsight

### Mobile

![PageSpeedInsight Mobile](/images/psi_mobile.JPG)

![PageSpeedInsight Mobile](/images/psi_mobile_time.JPG)

### Bureau

![PageSpeedInsight Bureau](/images/psi_bureau.JPG)

![PageSpeedInsight Bureau](/images/psi_bureau_time.JPG)

## Analyse de sécurité - wpscan

Interesting Finding(s):

[+] [Robot.txt](http://gmlb-et-ses-biobons.com/robots.txt)
*Interesting Entries:*

- /wp-admin/
- /wp-admin/admin-ajax.php

```txt
Found By: Robots Txt (Aggressive Detection)
Confidence: 100%
```

[+] [xmlrpc](http://gmlb-et-ses-biobons.com/xmlrpc.php)

```txt
Found By: Direct Access (Aggressive Detection)
Confidence: 100%
```

*References:*

- <http://codex.wordpress.org/XML-RPC_Pingback_API>
- <https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner>
- <https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos>
- <https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login>
- <https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access>

[+] [Readme](http://gmlb-et-ses-biobons.com/readme.html)

```txt
Found By: Direct Access (Aggressive Detection)
Confidence: 100%
```

[+] This site has 'Must Use Plugins': <http://gmlb-et-ses-biobons.com/wp-content/mu-plugins/>

```txt
Found By: Direct Access (Aggressive Detection)
Confidence: 80%
```

*Reference:*

[Must Use Plugins](http://codex.wordpress.org/Must_Use_Plugins)

[+] Upload directory has listing enabled: <http://gmlb-et-ses-biobons.com/wp-content/uploads/>

```txt
Found By: Direct Access (Aggressive Detection)
Confidence: 100%
```

[+] [WPCron](http://gmlb-et-ses-biobons.com/wp-cron.php)

```txt
Found By: Direct Access (Aggressive Detection)
Confidence: 60%
```

*References:*

- <https://www.iplocation.net/defend-wordpress-from-ddos>
- <https://github.com/wpscanteam/wpscan/issues/1299>
