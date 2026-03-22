# Architecture Data : SQL Server & Power BI.
Construction d'un pipeline de données automatisé sur SQL Server. Intégration de données commerciales et clients via une architecture Bronze-Silver-Gold pour générer des indicateurs de performance (KPIs) et des tableaux de bord décisionnels.

L'objectif du projet: 
Ce projet est né de la nécessité pour l'entreprise ParkAdventure de passer d'une gestion artisanale sur Excel à une architecture Data automatisée, afin d'identifier les leviers de croissance réels et de stopper la perte de clients.

Pour mettre fin à ce chaos, ma mission a été de construire une solution décisionnelle complète capable de :
-- Centraliser et Nettoyer : Créer une pipeline SQL (ETL) pour transformer des milliers de lignes de transactions "sales" en une base de données structurée et fiable.
-- Modéliser le Business : Traduire les règles métier (segmentation clients, rentabilité produits) directement dans le code pour automatiser les calculs complexes.
-- Piloter par la Donnée : Livrer un dashboard interactif permettant de passer d'une gestion artisanale sur Excel à une analyse stratégique en temps réel.

  1. Pilotage Exécutif & KPIs Globaux (Overview)
<img width="490" height="277" alt="image" src="https://github.com/user-attachments/assets/df8b8d56-f43f-4da4-b7b7-ff3746c1e048" />

J'ai structuré cette vue pour offrir une lecture instantanée de la santé financière. 
Elle repose sur mes jointures entre la table de faits gold.fact_sales et les tables de dimensions.

     -- Pilotage Global (Finances)
Indicateurs clés : Chiffre d'affaires total (29,35M€), volume de commandes (60K) et panier moyen.
Impact : Une vue temps réel sur la santé financière pour la direction.

     -- Analyse Clients (Marketing)
Segmentation : Répartition automatique des 18 480 clients en segments (VIP, Regular, New).
Fidélité : Calcul de la Récence (inactivité) pour identifier les clients à relancer avant qu'ils ne partent.

     -- Performance Produits (Stocks)
Top Ventes : Identification des produits "Champions" (la gamme Bikes génère 96% des revenus).
Optimisation : Analyse par catégorie pour éviter les ruptures de stock sur les modèles les plus rentables.



 2. Analyse des Clients & Segmentation (Fiche clients)

<img width="485" height="280" alt="image" src="https://github.com/user-attachments/assets/d08f19dd-ad0d-40dd-885f-d80b5b70082c" />
Ce tableau de bord permet de comprendre qui sont les 18 480 clients et comment ils consomment.

Segmentation Stratégique : Répartition automatique des clients en trois groupes (New, Regular, VIP) basée sur leur historique d'achat.
Indicateurs de Fidélité : Calcul de l'inactivité (Récence) en mois pour chaque client du "Top 10". Cela permet de repérer les gros acheteurs qui n'ont pas commandé depuis longtemps.
Démographie & Géo : Visualisation par tranche d'âge et par pays (domination du marché US à 40%).
Évolution Temporelle : Suivi des ventes par segment, montrant une forte accélération des nouveaux clients en 2013.


 3. Performance du Catalogue Produits (Fiche produits)

<img width="488" height="278" alt="image" src="https://github.com/user-attachments/assets/0ec70dad-a893-4422-982b-209aa72b8257" />

Ce tableau de bord analyse la rentabilité des 130 produits actifs.

Segmentation Produits : Classification automatique en trois catégories (High, Mid, Low Performer) selon le chiffre d'affaires généré.
Domination Catégorielle : Mise en évidence du segment Bikes qui représente 96,46% des revenus totaux.
Top 5 Produits : Identification des modèles "Champions" (gamme Mountain-200) pour prioriser les approvisionnements.
Analyse de l'Inactivité : Suivi du nombre de mois sans vente par produit pour identifier les références "dormantes" à déstocker.

