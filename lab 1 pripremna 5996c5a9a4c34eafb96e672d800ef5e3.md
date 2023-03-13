# lab 1 pripremna

1. What is the *Address Resolution Protocol (ARP)*, and what is its role in a network?
    - Komunikacijski protokol kojim se može doći do fizičke adrese (MAC) pomoću IP adrese.
2. What is a *Man-in-the-Middle (MitM)* attack, and how does ARP spoofing enable it?
    - Tip kriptografskog napada u kojem napadač se nalazi u sredini komunikacije te pokušava ubaciti neku svoju poruku unutar te komunikacije bez da primatelj zna, već on misli da mu to šalje prijatelj s druge strane komunikacije. ARP omogućuje da napadač odgovori svojom MAC adresom te tako zavara pošiljatelja.
3. How does an attacker use ARP spoofing to intercept network traffic?
    - Napadač pokušava falsificirati ARP zahtjev kako bi pošiljatelj podijelio svoju IP adresu s njim te se zatim napadač povezao sa svojom MAC adresom
4. How is the *cookie* used to derive the encryption/decryption key?
    - Kolačići sami po sebi ne koriste se izravno za izvodjenje ključa za enkripciju/dekripciju. Međutim, kolačići se mogu koristiti za pohranu podataka o sesiji i drugih podataka koji se koriste za generiranje ključeva za enkripciju.Međutim cookie može poslužiti
    tako da se key spremi unutar njega, a cookie će poslužiti tako da sakrije od svakog klijenta svoj sadržaj pa tako i sadržaj keya.
5. What REST API request do you need to send to the *crypto oracle* the secret cookie?
    - GET /arp/cookie
6. How do you obtain the authentication token?
    
    Trebate se autenticirati slanjem korisničkog imena (ime vašeg Docker *container*-a) i odgovarajuće lozinke.
    
    1.Registracija za račun s API-jem ili uslugom, ako je potrebno.
    2.Generiranje API vjerodajnica, poput API ključa ili pristupnog tokena, putem razvojnog portala API-ja ili usluge.
    3.Autentificiranje s API-jem ili uslugom koristeći svoje API vjerodajnice.
    4.Nakon uspješne autentifikacije, API ili usluga će izdati autentifikacijski token koji se može koristiti za slanje naknadnih API zahtjeva.
    
    
    
7. How do you use the authentication token to obtain the cookie?
    - Koraci za korištenje autentifikacijskog tokena za dobivanje kolačića ovise o određenom API-ju ili usluzi koja se koristi, i načinu na koji se kolačić upravlja u tom sustavu.
    Općenito, nakon što ste dobili autentifikacijski token, koristili biste ga za autentifikaciju s API-jem ili uslugom i slali naknadne zahtjeve za kolačić
    
8. What encryption mode is used to encrypt the challenge in this lab?
    - AES-CBC
9. What tool can you use to capture network traffic on a local network interface?
    - `tcpdump` ili Wireshark
