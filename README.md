# DevOps Project/Operations - persoonlijke opdracht 2e zittijd

- Student: Maximiliaan Muylaert
- Github-gebruikersnaam: [MaximiliaanM](https://github.com/MaximiliaanM)
- Github-repo: <https://github.com/HoGentTIN/p3ops-2122-2zit-MaximiliaanM>

Lees de [instructies](doc/instructies.md) voor de verwachtingen ivm het gebruik van deze repository!

## Inhoudstafel

### Documentatie:
- [Procedurehandleiding](doc/procedure.md)
- [Technische documentatie](doc/techhnische-documentatie.md)
- [Cheat sheet](doc/cheat-sheet.md)

### Broncode
- Lokale omgeving
  - [Playbook](src/ansible/site.yml)
  - [Build server host variabelen](src/ansible/host_vars/build.yml)
- Cloud-omgeving
  - [Playbook](src/cloud-vm/playbook.yml)
  - [inventory file](src/cloud-vm/inventory)
- Docker
  - [Dockerfile](src/ansible/files/Dockerfile)
  - [docker-compose](src/ansible/files/docker-compose.yml)
