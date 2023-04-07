# DOCKER ENGINE 

	1. Decouvete de socket sous linux
		- socket type UNIX qui permet la communication entre deux programme locals
		- socket type TCP qui permet la communication entre deux programme appartenant a des machine diff
		- soket type UDP utilise les deux 
	2. Creation des des socket avec la commande `nc`
		- `nc -l [port]` creation du serveur 
		- `nc [machine] [port]` creation de la machine d ecoute
		- `nc -u` pour les communication udp

	3. Fichier de configuration 
		- /var/run/socket.s ** fichier de socket **

	4. Commande utiles 
		- `ss` liste de ports de la machine
		- `curl` client pour la communication sur une socket 
			* `curl -GET /var/run/socket.socs https://localhost:2375/images/json | jq`

