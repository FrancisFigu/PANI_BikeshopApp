[<< liste d'écrans](02-analyse-fonctionelle.md#link01) 

[<< scenarios](04-scenarios.md) 

# Schéma de la base de données # 

<img src="./images/img-database-v4.png" alt="Alt text" style="height:600px;">

 - Table ‘rental’ : Cette table stocke les informations de chaque location, incluant un identifiant unique, la date de début, la date de fin et l’identifiant du client concerné.  Cette table est liée à la table ‘bicycle’ via la table ‘bicycle_rental’ car il s’agit d’une relation ‘many to many’ ; plusieurs vélos peuvent se trouver dans une location, ainsi que plusieurs locations peuvent être liées à un vélo. 

 - Table ‘bicycle’ : Cette table stocke les informations des différents vélos de la flotte, incluant un id unique, des informations concernant le type de vélo et 3 clés étrangères : ‘manufacturer_id’, ‘shop_id’ et ‘price_rate_id’. 

 - Table ‘manufacturer’ : Cette table stocke les informations liées aux différents fabricants des vélos qui se trouvent dans la flotte. Ces données facilitent la gestion de réparation et l’achat de pièces de réparation et le suivi de la garantie. 

 - Table ‘shop’ : Cette table contient les coordonnées de chaque magasin. 

 - Table ‘price_rates’ : Cette table contient les différents types de prix en fonction de la saison et la durée de la location et le type de vélo. Il existe des prix pour la location de vélos ainsi que pour la location des accessoires. 

 - Table ‘accessory’ : Cette table contient les informations des accessoires, incluant le type et un id unique.  Cette table est liée à la table ‘rental’ via la table d’association ‘accesory_rental’ car il s’agit d’une relation ‘many to many’ ; plusieurs accessoires peuvent se trouver dans une location, ainsi que plusieurs locations peuvent être liées à un accessoire. 

- Table ‘client’ : Cette table contient les données du client. 

[<< scenarios](04-scenarios.md) [class diagram >>](06-class-diagram.md) 
