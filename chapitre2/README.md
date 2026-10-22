Chapitre 2 - Exemple Prof - Architecture Darna Market Variante D
Choix de plateforme justifié (5 lignes)
Voir grille-choix-D.md
Score: WooCommerce 4.9/5 retenu pour D. Coût zéro, compétences WP, contrôle données Tunisie, modules ClicToPay/Konnect existants, lancement 1 semaine. Shopify écarté: abonnement en devise + données à l'étranger + passerelle redirection difficile.

Schéma architecture
Fichier: architecture-darna-D.drawio + export PNG à faire
3 couches: Vitrine (WordPress+Woo), Admin (/wp-admin), Services (MariaDB, Paiement, Transport, WhatsApp)
Flux: 1 HTTPS vitrine, 2 HTTPS admin, 3 SQL DB, 4 API ClicToPay (ROUGE), 5 Webhook paiement (ROUGE - sécuriser), 6 API Aramex, 7 WhatsApp Click&Collect
Acteurs: Client, Gestionnaire, Transporteur, Banque/Passerelle

TP2 Docker
docker-compose.yml fourni. Lancer: docker compose up -d, ouvrir localhost:8080, installer WP + WooCommerce, créer 3 produits (ex: set poterie Sejnane 90TND, eau rose Zaghouane 25TND, atelier 30TND), captures vitrine + /wp-admin

Sécurité: changer mots de passe ChangeMe! -> .env, ne jamais déposer sur GitHub

Livrables semaine: Schéma .drawio + image, Grille choix, Captures boutique ou compte rendu si Docker impossible
