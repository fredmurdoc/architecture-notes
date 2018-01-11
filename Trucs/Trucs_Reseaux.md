Trucs Réseaux
=============


## Tunnels SSh




ssh -R port-distant:HOSTNAME:port-local  machine-distante


ssh -L port-local:HOSTNAME:port-distant machine-distante




creation d'un serveur local qui pointe vers une cible

ssh -L PORT:Serveur cible:portcible serveur_qui_accede


### Exposittion d'un serveur interne vers un autre serveur d'une autre zone reseau

Le serveur HTTP slnxcnamtsgitlab01.ntes.fr.sopra doit être accessible a partir du serveur rahan


localhost se tansofrme en serveur sur le port 1234 pour pointer vers le serveur slnxcnamtsgitlab01 (mon poste n'a pas de serveur ssh mais slnvmrt06 sert d'intermediaire)

ssh -L 1234:slnxcnamtsgitlab01.ntes.fr.sopra:80 slnvmrt06

je crée un tunnel qui permet à rahan d'accèder à mon service via le port de rahan 12345

ssh -R 12345:localhost:1234 mowda10@rahan.cnqd.cnamts.fr


ssh -L 12346:rahan.cnqd.cnamts.fr:12345 mowda10@rahan.cnqd.cnamts.fr


wget http://localhost:12345

