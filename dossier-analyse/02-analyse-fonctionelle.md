[<< introduction](01-introduction.md) 
# Analyse fonctionnelle # 

## Description générale BikeRentApp ## 

Les fonctions principales de l’application de gestion de locations de vélos sont : 

- Gérer les réservations   

- Gérer les payements 

- Montrer en temps réel la disponibilité 

- Montrer en temps réel l’état de chaque vélo 

- Notifier tous les acteurs à chaque étape 

Sur le diagramme UML ci-dessous, il est possible de visualiser le processus fonctionnel principal que l’application prendra en charge : 


````mermaid
 flowchart TD
    A(booking)
    -->B(payement)
    -->C(bike ready for pick-up)
    -->D(rental)
    -->E(drop-off & check)
E-->C
    E-->G(extra payements)
    E-->F(repair)
    F-->C

````
## Utilisateurs ## 

Les utilisateurs de l’applications sont : 

- ### L’utilisateur client : ### 
  Qui utilise l’application pour faire la réservation et le payement de la location d’un ou plusieurs vélos.  

- ### L’utilisateur collaborateur du magasin : ###
  Qui utilise le calendrier de locations pour organiser son travail et préparer les vélos à louer.  

- ### L’utilisateur administrateur : ###
  Qui gère les flottes de vélos et les magasins où les vélos se trouvent.

## Ecrans ## 

- ### Liste d'ecrans du client ### 

  - Create account 
  - Sign-in 
  - Dashboard
  - Profile
  - Choose dates 
  - Choose location 
  - Choose bike 
  - Confirm 
  - Cancel a booking 
  - Notify a problem 


<img src="./images/img-create-account.png" alt="Alt text" style="height:300px;"><img src="./images/img-log-in.png" alt="Alt text" style="height:300px;"><img src="./images/img-dashboard.png" alt="Alt text" style="height:300px;"><img src="./images/img-profile.png" alt="Alt text" style="height:300px;"><img src="./images/img-choose-date.png" alt="Alt text" style="height:300px;"><img src="./images/img-choose-location.png" alt="Alt text" style="height:300px;"><img src="./images/img-choose-bike.png" alt="Alt text" style="height:300px;"><img src="./images/img-confirm.png" alt="Alt text" style="height:300px;"><img src="./images/img-cancel.png" alt="Alt text" style="height:300px;"><img src="./images/img-notify-problem.png" alt="Alt text" style="height:300px;">

- ### Liste d'écrans du collaborateur du magasin ### 

  - Dashboard
  - Page vélo 
  - Page réservation
  - Page profil client

<img src="./images/img-dashboard-magasin2.png" alt="dashboard magasin" style="height:350px;"><img src="./images/img-page-bike.png" alt="page bike" style="height:350px;"><img src="./images/img-page-booking.png" alt="page booking" style="height:350px;"><img src="./images/img-profil-client.png" alt="Alt text" style="height:350px;">

- ### Liste d’écrans du manageur ###

  - Dashboard 
  - Page magasin
  - Page vélo 
  - Page réservation 
  - Page profil client 
  - Page modification vélo 
  - Page création profil vélo 

[>> backlog](03-backlog.md) 
