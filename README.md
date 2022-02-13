## Kata-Potter project 👋

### List of participants
- ⚡ Quentin Cheruel
- ⚡ Loïc Robin
- ⚡ Lucas Belin
- ⚡ Alexandre Tison

<br/>

### Versions
- Jenkins: 2.319.2
- Nexus: 13.5.0-debian-10-r81
- Sonarqube: 9.3.0-debian-10-r4
- PostgreSQL: 13.5.0-debian-10-r81

<br/>

### Identifiers used for each volume
- Jenkins: (UserName) Jack (Password) root

<br/>

If needed, you can execute this commands if the pipeline crash (maven not reconized):
docker exec -it -u root desktop-jenkins-1 bash |
apt-get update |
apt-get install maven
