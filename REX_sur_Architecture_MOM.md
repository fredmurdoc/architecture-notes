REX sur Architecture MOM
========================


## separation et reponsabilisation des chaines de messages

Les chaines de messages doivent être séparée sur leurs évènements de mise à jour.

Ex :  un empileur qui stocke des evenements. Un depileur pour depileur les evenements selon la capacité de traitements.
On a bien 2 responsabilités :  consommer, et traiter dans des conditions les evenements

Objectifs : 
 - pouvoir mettre à jour des chaines de façon indépendantes
 - pouvoir administrer des chaines de façons indépendantes
