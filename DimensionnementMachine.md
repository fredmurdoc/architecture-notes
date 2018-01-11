Dimmensionnement Machine
========================


#Cpu vs. Core

Un Core est un unité basique d'exécution.

Un CPU peut être composé de plusieurs Cores.

La capacité de traitement d'un CPU est donc égale en temps simultané à 
X = number cores * number of HW-threads per core.


Un vCPU est géré par l'hyperviseur. L'hyperviseur se débrouille pour trouver de la ressource CPU pour y faire executer le processus.

Attention, demander plus de vCPU ne signifie pas une amélioration des performances :  en effet, plus il y a de vCPU plus il y a de travail de routage vers les ressources pour l'hyperviseurs.



#Dimensionner une Machine Virtuelle

Ternir compte des system requirements de l'OS