# Mpd
A MPD radio

 https://www.musicpd.org/
 
 1- Radio
 
 ![01_Radio.jpeg](/Picts/01_Radio.jpeg)

J'ai trouvé ce petit poste de radio pour quelques Euros dans un bel endroit au coeur de la  Normandie. 
Ce récepteur à certainement ecouté de belles émissions sur les grandes ondes ou petites ondes (valeur) mais de nos jours, le monde entier s'ouvre aux diffusions numériques. Il ne faut pas oublier non plus la collection d'albums numériques aux formats FLAC, OGG... (ne parlons pas du MP3)

#sortiedusinemorgny
#vintageradio
#raspberrypi



2 - Raspberry

 ![02_Raspi.jpeg](/Picts/02_Raspi.jpeg)

Le coeur de ma radio numérique sera un Raspberry 3b trouvé dans mon placard (geek hunt). J'y ajouterai MPD (Music Player Deamon) qui fera tout le travail de décodage des fichiers.
#vintageradio
#raspberrypi


à suivre... mettre le nb de post




3 - je suis retourné sur les sites Linux afin de ré-apprendre le montage des disques sous Linux. Avec Raspberry, les disques USB sont la seule solution à ma connaissance. Ma collection de musique est sur un "petit" disque usb de 1To. Les capacité évoluent si vite. Je me souviens de mon premier PC avec un disque de 340 Mo. le Montage automatique du disque est documenté ici : 
https://www.raspberrypi.org/documentation/configuration/external-storage.md
Pensez à détecter le disque avec son numéro UUID, cela assure le montage de la façon la plus sûre.

Formatage avec fdisk






4 -
Sauvegarder la carte micro SD. 
sur mon MacBook, la commande pour sauvegarder ma carte est :

dd if=/dev/disk2 of=/Volumes/USB/BackupSD.dmg

ce qui permet de conserver un backup. J'ai vu que sur les dernière version de Raspbian, une commande existe pour faire une sauvegarde régulière de la carte.
Le mieux serait quand même de bosser sur le disque dur





5 - j'ai ajouté un bouton pour éteindre le raspberry. En effet, cette carte n'en possède pas et vous devez débrancher la prise. (Apple le ferait aussi sur les ATV...)
LA carte SD ne supportera pas cela longtemps et il vaut mieux lancer une commande "sudo halt". Ceci est fait avec le contrôle d'une broche GPIO et un petit script.
j'ai trouvé cela ici et c'est bien documenté : https://howchoo.io/2RlyZIm
#howchoo






4 - installation de MPD, photo d'écoute en ligne de commande

![04_MPC_teminal.mov](/Picts/04_MPC_teminal.mov)

C'est facile (d'un point de vue informatique) de lire un fichier : MPC PLAY, MPC STOP, MPC NEXT ... tout est bien documenté

https://www.musicpd.org/

mpc is a command-line client for the Music Player Daemon (MPD). It connects to a MPD and controls it according to commands and arguments passed to it. 




6 - un petit écran LCD pour afficher le titre de lecture


7 - je sèche sur le code Python pour lire le titre en cours de lecture. Après quelques recherche, #mark weller à parfaitement documenté ceci et donne un beau script très efficace


http://www.markwheeler.com/wordpress/?p=557










5 - j'ajoute 




