# i-Educar Relatórios

Módulo de relatórios para o [i-Educar](https://github.com/uaefama/i-educar).

## Dependências

Os relatórios utilizam a biblioteca [JasperReports](https://community.jaspersoft.com/project/jasperreports-library)
desenvolvida em Java para renderizar os arquivos em PDF.

Para intermediar a conexão entre PHP e Java é utilizada a biblioteca [JasperStarter](http://jasperstarter.cenote.de/).

- PHP ter permissão para executar as funções `exec` e `passthru` no servidor.
- [OpenJDK](https://openjdk.java.net/) 8 instalado no servidor.

## Instalação

> Para usuários Docker, executar os comandos `# (Docker)` ao invés da linha seguinte.

Clone este repositório a partir da raiz do i-Educar:

```bash
git clone git@github.com:uaefama/i-educar-reports-package.git packages/uaefama/i-educar-reports-package
```

Ative o pacote via plug and play:

```bash
# (Docker) docker-compose exec php composer plug-and-play
composer plug-and-play
```

Instale o pacote:

```bash
# (Docker) docker-compose exec php artisan community:reports:install
php artisan community:reports:install
```

Publique os assets:

```bash
# (Docker) docker-compose exec php artisan vendor:publish --tag=reports-assets --ansi
php artisan vendor:publish --tag=reports-assets --ansi
```

---
