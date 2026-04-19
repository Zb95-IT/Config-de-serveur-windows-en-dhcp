## Objectif
Mise en place d’un serveur DHCP sur Windows Server avec :

- une adresse IP statique sur le serveur : `172.20.0.1/24`
- une étendue DHCP : `172.20.0.100` à `172.20.0.200`
- un client recevant une adresse automatiquement par DHCP
- une réservation DHCP pour un second client en `172.20.0.10`

## 1. Configuration de l’étendue DHCP sur le serveur

Cette capture montre la configuration de l’étendue DHCP sur le serveur Windows.  
On voit que le pool d’adresses distribué va de **172.20.0.100** à **172.20.0.200**.
 
<img width="721" height="410" alt="image" src="https://github.com/user-attachments/assets/038c5fd5-2a24-4e08-aec4-d0bd1cf269f8" />

## 2. Configuration IP du premier client

Cette capture montre que le premier client est bien configuré en **DHCP** et qu’il a reçu automatiquement une adresse IP dans l’étendue prévue, ici **172.20.0.100**.


<img width="737" height="681" alt="image" src="https://github.com/user-attachments/assets/6fd5323e-9871-4ed4-b913-f1ef1db3bdbd" />
<img width="1713" height="700" alt="image" src="https://github.com/user-attachments/assets/508a1859-d52d-4136-89ff-e074bf1c2dd2" />

## 3. Réservation DHCP et attribution statique au second client

Cette capture montre la **réservation DHCP** créée sur le serveur pour le second client, ainsi que la configuration IP obtenue côté client après renouvellement du bail.  
Le client reçoit bien l’adresse réservée **172.20.0.10**.


<img width="1713" height="700" alt="image" src="https://github.com/user-attachments/assets/508a1859-d52d-4136-89ff-e074bf1c2dd2" />
<img width="737" height="681" alt="image" src="https://github.com/user-attachments/assets/6fd5323e-9871-4ed4-b913-f1ef1db3bdbd" />

