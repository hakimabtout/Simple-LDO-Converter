# Simple-LDO-Converter
Conception d'un module d'alimentation compact basé sur le régulateur LDO MIC5317 (150mA, 2.5V-6V). Inclut schémas, typon et documentation technique.

## Présentation
Le MIC5317 est un régulateur de tension à faible chute (LDO) haute performance, idéal pour les appareils portables. Il peut fournir jusqu'à **150 mA** avec une consommation de courant très faible.

## Caractéristiques Techniques
* **Tension d'entrée :** 2,5V à 6,0V
* **Tension de sortie :** (Selon modèle, ex: 3,3V)
* **Courant de sortie max :** 150 mA
* **Courant de repos :** 29 µA (typique)
* **Condensateurs requis :** 1 µF en entrée et en sortie (céramique)

## Brochage (Boîtier SOT23-5)
| Broche | Nom | Fonction |
| :--- | :--- | :--- |
| 1 | **VIN** | Entrée d'alimentation |
| 2 | **GND** | Masse |
| 3 | **EN** | Activation (Niveau Haut = ON / Bas = OFF) |
| 4 | **NC** | Non connecté |
| 5 | **VOUT** | Sortie régulée |

## Liste des composants (BOM)
* **U1 :** MIC5317 (SOT23-5 ou UDFN)
* **C1 :** Condensateur céramique 1 µF (Entrée)
* **C2 :** Condensateur céramique 1 µF (Sortie)

## Recommandations de design
* Placer les condensateurs **C1** et **C2** le plus près possible du circuit intégré.
* Utiliser un plan de masse large pour la dissipation thermique.
* Ne pas laisser la broche **EN** flottante (la relier à VIN si toujours actif).

## Structure du dépôt
* `/schematics` : Schémas électriques.
* `/pcb` : Fichiers de routage (Gerber).
* `/docs` : Documentation technique (Datasheet).
