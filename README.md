# Generate_Reporting_App
# Automate d'Extraction et d'Export de Données en C#

Cet automate en C# a été conçu pour accéder à une base de données, extraire des données de la table `Tbl_Pli` associées à chaque client par code de traitement, et les insérer dans une base de données client. En outre, il génère un rapport CSV avec la même structure que la table `Tbl_Pli` à chaque lancement de l'automate (une fois par jour).
Les exports effectués de la base générale vers la base client sont également tracés dans une table `Tbl_Trace` avec un identifiant d'export Id_Export.
Une fois les plis pour un code de traitement de meme client sont insérés, et lors des prochains passage, si la durée de retention de ces plis est dépasée (on le fixe en passant les paramétre sde traitement en amont et sous la demande du client) , ces plis seront prugés.

## Instructions d'Installation

1. Clonez le référentiel sur votre machine locale :

```bash
git clone https://github.com/ingouday/automate-extraction-csharp.git

Utilisation
Exécutez l'automate une fois par jour (ou via une tache plannifiée autant qu'on veut).

Les données extraites de la table Tbl_Pli seront automatiquement insérées dans la base de données client.

Un rapport CSV sera généré à chaque exécution, suivant la structure de la table Tbl_Pli.

Les traces des exports de la base générale vers la base client seront enregistrées dans la table Tbl_Trace.

Contributions
Les contributions sont les bienvenues ! Si vous souhaitez améliorer cet automate, n'hésitez pas à ouvrir une demande de pull
