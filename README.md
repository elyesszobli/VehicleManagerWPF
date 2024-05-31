## UML Schema

``` mermaid
classDiagram

        class Agence{
            - Nom : string
            - Adresse : string
            - ListeVehicule : Vehicule
        }

        class Vehicule{
            <<Abstract>>
            - Immatriculation : string
            - Marque : string
            - Modele : string
            - Annee : int
            - Prix : double
            + AjouterVehicule() : void
            + ModifierVehicule() : void
            + SupprimerVehicule() : void
        }

        class Voiture {
            - TypeCarburant : string
            - NombrePortes : int
            - Puissance : int
            - Transmission : string
        }

        class Moto {
            - Cylindree : int
            - NombreDeCylindres : int
            - Type : string
            - ABS : bool
        }

        Vehicule <|-- Voiture
        Vehicule <|-- Moto

        Agence "1"*--"n" Vehicule 
```