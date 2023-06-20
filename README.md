# ansibleesercizio2
Made a playbook that connect to Windows via WinRm , install some chocolatey's package,change hostname and install and configure ISS on a different port and hostname.As a final step create some logs about playbook's status run

Esercizio Ansible #2
Requisiti

VM Windows Server 2016 con a bordo il tool chocolatey per l'installazione dei pacchetti
Utente: Administrator
Password: Cognome123!
IP: _____._____._____._____

Il server viene fornito già configurato per essere raggiungibile via WinRM (su porta 5986 con certificato self-signed) per accesso tramite Ansible e RDP per accesso grafico.
VSCode
WSL 2 - Ubuntu 22.04
Ansible (ultima release)


Base: realizzare un playbook Ansible che si connetta al server via WinRM e applichi le seguenti configurazioni:

Prima di procedere, comunicare ad uno degli amministratori che si sta iniziando a lavorare sull'istanza, in modo che possano effettuare uno snapshot per ripristinare eventualmente la VM in caso di problemi;
Modificare l'hostname a "vm-cognome" e riavviare il server se necessario;
Installare il web server IIS (Internet Information Services) di Microsoft mediante le funzionalità di Windows Server;
Installare 7zip, notepad++ e Chrome all'ultima release mediante il tool chocolatey;
Ogni tanto questo passaggio può dare errore, come gestirli in Ansible?
Il web server IIS viene fornito con un sito web di default, modificarne la configurazione in modo che risponda sulla porta 8888 e che il sito sia raggiungibile solo se chiamato con FQDN fake-site.mycompany.com (binding);
Tip: per testare il funzionamento ti serve davvero un record DNS?
Come ultimo step del playbook creare un file di log all'interno del server nel percorso "C:\<UUID RANDOM>_deploy.log" con il seguente contenuto:

Ansible Version: <VERSIONE DI ANSIBLE>
OS Version: <VERSIONE OS>
Ora completamento: <DATA-ORA ATTUALE>
