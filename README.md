# Moving between Git
Creem un perfil en el Github i ens creem un repositori

Entrar en el directori on volem crear la carpeta repositori en el PC

Terminal:

pau@pau-LIFEBOOK-T904:~ cd Escritorio/
pau@pau-LIFEBOOK-T904:~/Escritorio cd Master\ en\ Robotica/
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica cd Robotics\ Integration/
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration

#En aquest cas ja hem arribat a la carpeta on volem crear el repositori

#Per crear la carpeta "Repositori" i entrar en aquesta fem la següent comanda

mkdir repo_paumila && cd repo_paumila // Aquesta comanda crearà la carpeta repo_paumila en el directori on estem actualment "/Escritorio/Master en Robotica/Robotics Integration" i entrara dins la carpeta per poder realitzar més comandes

#A continuació fem una serie de comandes per inicialitzar el respositori amb el Github

Terminal:

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila$ git init --bare
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila$ git clone https://github.com/Paumila/Classe1.git

#En aquest cas ens ha creat el repositori que hem creat en el Github dins el repositori del nostre ordinador. 

#Entrem dins la carpeta del repositori del Github, en el meu cas Classe1

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$

#Creem un fitxer1 en el repositori Classe1 i realitzem una serie de comandes per poder pujar en el repositori de Github el fitxer

Terminal:

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git add fitxer1
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git commit -am "Pujar fitxer1"
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git push origin master

#Ens demana el Username i el Password

Username for 'https://github.com': Paumila
Password for 'https://Paumila@github.com': 

#Si fem la comanda "git status" podem saber si esta actualitzat tot al Github

#Si volem esborrar un fitxer s'ha de fer de la seguent manera, creem un fitxer dins la carpeta Classe1 que es digui fitxer 2

#Tornem a fer tot el proces explicat anteriorment per pujar aquest fitxer en el Github, un cop realitzat el proces de "Push" realitzem el seguent per fer el borrat del fitxer

Terminal:

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git rm fitxer2
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git status
En la rama master
Tu rama está actualizada con 'origin/master'.

Cambios a ser confirmados:
  (usa "git reset HEAD <archivo>..." para sacar del área de stage)

	borrado:        fitxer2

#En aquest punt podem veure com el fitxer esta borrat pero no actualitzat en el Github

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git commit -am "Fitxer2 borrat"
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git push origin master

#En aquest moment el fitxer2 ja esta esborrat del Github

#Ara modifiquem un dels fitxers (Afegint algo dintre del fitxer) i el pujarem al Github

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git commit -am "Afegit Adeu"
[master 2ae2898] Afegit Adeu
 1 file changed, 1 insertion(+) //Podem veure com s'ha modificat el fitxer i s'ha afegit un text dins el fitxer
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git push origin master

#Ara crearem una nova branca

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git checkout -b carrot
Cambiado a nueva rama 'carrot'

#Creem un fitxer3 i el pujarem en aquesta branca

pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git add fitxer3
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git commit -am "Pujar fitxer 3 en branca Carrot"
pau@pau-LIFEBOOK-T904:~/Escritorio/Master en Robotica/Robotics Integration/repo_paumila/Classe1$ git push origin carrot

#En aquest punt ja tenim la branca carrot creada amb el fitxer 3 pujat en el Github 
