
# Liste de Scénarios # 
## 1.- Réservation de locations – utilisateur client # 
### Préconditions : ### 

 - Le client a déjà un compte 
 - Le client est authentifié 
````mermaid
 flowchart TB
    A(dashboard client)
    -->B(choose date)
    -->C(choose location)
    -->D(choose bike)
    D-->F(confirm)
-->G(proceed to payement)
F--|re-start|-->B
F--|add|-->D
````
### Séquence d’écrans : ###
<img src="./images/img-dashboard.png" alt="Alt text" style="height:300px;"><img src="./images/img-choose-date.png" alt="Alt text" style="height:300px;"><img src="./images/img-choose-location.png" alt="Alt text" style="height:300px;"><img src="./images/img-choose-bike.png" alt="Alt text" style="height:300px;"><img src="./images/img-confirm.png" alt="Alt text" style="height:300px;">

 - Dashboard : Client commence le processus en sélectionnant ‘add booking’ 
 - Step 1 : Client sélectionne les dates sur le calendrier 
 - Step 2 : Client sélectionne le magasin 
 - Step 3 : Client choisi un vélo  
 - Step 4 : Pour finir, l’utilisateur est amené sur une page résumée (panier), à partir d’où il est possible d'annuler (recommencer), ajouter un vélo ou bien confirmer et passer au processus de payement. 

### Postconditions : ### 

 - Le client est mené au processus de payement 
 - Si le processus de payement est complété correctement, des notifications sont envoyées tant vers le client que vers le magasin 

### Règles métier : ### 

 - La date de début de la location doit être plus petite que la date de fin 
 - Le nombre de vélos choisis ne doit pas dépasser le nombre de vélos disponibles pour location dans les magasins pour les dates sélectionnées.

## 2.- Changement de statut ‘available’ <--> ‘in-repair’ – utilisateur collaborateur du magasin ## 

### Préconditions : ###  

- Le magasin est authentifié
- Le vélo a été ajouté au pool de vélos de location
````mermaid
 flowchart TB
    A(dashboard magasin)
    -->B(sélectionne vélo)
    -->C(change statut à 'in-repair')
    C-->A
    B-->D(change statut à 'available')
    D-->A

````
### Séquence d’écrans : ###
<img src="./images/img-dashboard.png" alt="Alt text" style="height:300px;">

- Collaborateur sélectionne le vélo sur le dashboard 
- Collaborateur change le statut à ‘in-repair’ sur la page du vélo 
- Collaborateur change le statut à ‘available’ sur la page du vélo 

### Postconditions : ### 

- Le vélo est remis en statut ‘disponible'. 

### Règles métier : ### 

- Le collaborateur doit pouvoir changer le statut d’un vélo à n’importe quel moment 
- Au moment où le vélo est mis en statut ‘in-repair’ le système doit enlever ce vélo du pool de vélos disponibles. 
- Au moment où le vélo est remis en statut ‘disponible’ le système doit ajouter ce vélo dans le pool de vélos disponibles. 
