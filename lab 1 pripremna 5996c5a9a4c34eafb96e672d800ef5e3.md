# lab 1 pripremna

1. What is the *Address Resolution Protocol (ARP)*, and what is its role in a network?
    - Komunikacijski protokol kojim se može doći do fizičke adrese (MAC) pomoću IP adrese.
2. What is a *Man-in-the-Middle (MitM)* attack, and how does ARP spoofing enable it?
    - Tip kriptografskog napada u kojem napadač se nalazi u sredini komunikacije te pokušava ubaciti neku svoju poruku unutar te komunikacije bez da primatelj zna, već on misli da mu to šalje prijatelj s druge strane komunikacije. ARP omogućuje da napadač preuzme IP adresu pošiljatelja te zbog toga dobije ARP zahtjev.
3. How does an attacker use ARP spoofing to intercept network traffic?
    - Napadač pokušava falsificirati ARP zahtjev kako bi pošiljatelj podijelio svoju IP adresu s njim te se zatim napadač povezao sa svojom MAC adresom
4. How is the *cookie* used to derive the encryption/decryption key?
    - Tako da se spremi sami key unutar cookie, a cookie će poslužiti tako da sakrije od svakog klijenta svoj sadržaj pa tako i sadržaj keya. username & password ⇒ token ⇒ **cookie**
     ⇒ key ⇒ Chuck Norris fact
5. What REST API request do you need to send to the *crypto oracle* the secret cookie?
    - GET /arp/cookie
6. How do you obtain the authentication token?
    
     trebate se autenticirati slanjem korisničkog imena (ime vašeg Docker *container*-a) i odgovarajuće lozinke:
    
    `POST username=my_name&password=my_pass /arp/token`
    
7. How do you use the authentication token to obtain the cookie?
    - Treba prvo potvrditi svoj identitet da bi mogli pristupiti cookieu, a to ćemo obaviti
    
    pomoću authentication tokena.
    
8. What encryption mode is used to encrypt the challenge in this lab?
    - AES-CBC
9. What tool can you use to capture network traffic on a local network interface?
    - `tcpdump`