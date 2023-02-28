# GIT-intro

In deze repository vind je informatie om te starten met GIT CLI.

### GitHub sleutel
* Ga naar GitHub, klik op je account-foto rechtsboven.
* settings
* Links onderaan zie je staan 'developer settings'
* Personal Access Tokens
* Tokens (Classic)
maak een token, geef deze een naam, geef toestemming om repo te gebruiken. Je krijgt een code. NIET AFSLUITEN
                         
Ga naar de command line. Navigeer naar documenten. Maak een nieuwe map 'gh' 
de commando's die je nodig hebt zijn:

``` bash
pwd       print working directory                                             
ls -l     toont de bestanden in de directory
cd ..     naar bovenliggende directory
cd <dir>  ga naar de directory dir
mkdir gh  maak een directory gh
```

Maak een map "sleutels", maak een bestand aan met nano waarin je de huidige sleutel kopieert.

``` bash

mkdir sleutels
nano sleutel23 
```
Kopieer de sleutel vanuit de browser (GitHub), en plak deze in dit bestand, zonder er iets ander bij te zetten.
Plakken doe je met ctrl + shift + v
afsluiten doe je met ctrl + x, druk op j als je wilt saven, enter om op te slaan.

### Installeer GH CLI

type in de command line:

``` bash
type -p curl >/dev/null || sudo apt install curl -y
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg \
&& sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```
Daarna:
``` bash
sudo apt update
sudo apt install gh
```
type uw passwoord indien gevraagd.

### inloggen in GH CLI 
Zorg dat je in de directory bent, waar het sleutelbestand aanwezig is. 
Type onderstaande code, ipv mytoken.txt geef je de naam in van jouw sleutelbestand.

``` bash
$ gh auth login --with-token < mytoken.txt
```

### Gebruik ghCLI voor de eerste keer.
Ga naar de directory '~/Documenten/gh'

We gaan eerst kijken welke repositories we onder onze account hebben, daarna gaan we de repository 'bash_tutorial' downloaden.


``` bash
gh repo list
gh repo clone <repository> [<directory>] [-- <gitflags>...]
```
bij repository type je de naam van de repository in, je hoeft je user-name niet over te nemen.
Je downloadde alle bestanden van de repository in deze map!
Goed gedaan!
Je kan starten met de volgende les.
