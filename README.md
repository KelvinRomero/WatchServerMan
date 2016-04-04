# WatchServerMen Backup

Who watch the servers? And how you make backups?

## Created by

Kelvin Romero

## Funcionalidades / Usabilidade

  Passos para configurar e realizar backups:
  - Instalar aplicação (Mais abaixo)
  - Acessar interface web
  - Realizar login
  - Seleciona as pastas para gerar backups
  - Escolhe o destino do backup

### Bacukps

Através de uma interface Web simplificada é possível adicionar servidores e configurar os arquivos CRON para gerenciamento de backups.

- Customização
- Agendamento *
- Criação
- Remoção *
- Listagem *

*Em breve

### Instalação

Para instalar esta aplicação deve-se obter inicialmente o vagrant e o virtual box.

Então o primeiro passo consiste em copiar o projeto através do comando:

```
$ git clone url
```

Toda a configuração do servidor será feita através do Vagrantfile. Basta executar o comando abaixo:

```
$ vagrant up
```
