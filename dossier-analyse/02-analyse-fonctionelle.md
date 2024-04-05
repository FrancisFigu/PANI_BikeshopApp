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
    A(client selects dates) 
    --> B(client selects bike
    available for the selected dates)
    -->C(client selects available location)
    -->D(payement process)
    D-->E(bike shop booking notification/ 
    add on rental calendar)
    D-->F(client booking/
    payement confirmation)
    E-->G
    F-->G(shop confirms pickup)
    G-->H(rental period)
    H-->I(return date)
    I-->J(return confirmation)
    J-->K(bike check)
    K-->M(damaged)
    M-->N(extra fees notification)
    I-->j(no return confirmation)
    j-->k(alert message to client & shop)
    k-->l(extra fees notification)
    l-->J
    N-->O(bike to in-repair status)
    O-->L
    N-->P(extra fees payement process)
    L--|bike to available status|-->B
    K-->L(bike OK status)

````
