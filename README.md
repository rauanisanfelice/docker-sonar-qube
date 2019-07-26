![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/rauanisanfelice/sonar-qube.svg)
![GitHub top language](https://img.shields.io/github/languages/top/rauanisanfelice/sonar-qube.svg)
![GitHub pull requests](https://img.shields.io/github/issues-pr/rauanisanfelice/sonar-qube.svg)
![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/rauanisanfelice/sonar-qube.svg)
![GitHub contributors](https://img.shields.io/github/contributors/rauanisanfelice/sonar-qube.svg)
![GitHub last commit](https://img.shields.io/github/last-commit/rauanisanfelice/sonar-qube.svg)

![GitHub stars](https://img.shields.io/github/stars/rauanisanfelice/sonar-qube.svg?style=social)
![GitHub followers](https://img.shields.io/github/followers/rauanisanfelice.svg?style=social)
![GitHub forks](https://img.shields.io/github/forks/rauanisanfelice/sonar-qube.svg?style=social)
<!------------------------------->
# SONAR QUBE

Template do sistema Sonar Qube para realizar testes de qualidade no código.

<!------------------------------->
## Para implementar o ambiente você precisa seguir as seguintes etapas:


1. Criar todos os containers;
    1. Configurando container PGADMIN;
2. Configurando Sonar Qube;
    1. Acessando;
    2. Atualizando Plugins;
3. Instalando Sonar Scanner;
4. Exec;
5. Links importantes;

<!------------------------------->
## 1. **Criar todos os containers;**

São 3 containers que serão criados:

* SONAR_POSTGRE;
* SONAR_PGADMIN;
* SONAR_QUBE;

Para maiores detalhes dos containers:
```
docker-compose.yml
```

```dockerfile
docker-compose up -d
```

<!------------------------------->
### 1. **Configurando container PGADMIN;**

Acesse o link:

http://localhost:16000

Realize o login:
>User: rauanishida@squads.gs  
>Pass: docker123

Clique em: Create > Server

Conecte no Banco com os seguintes parametros:  

Name: #nome desejado#  
>Host: sonar-postgre 
>Port: 5432  
>Db  : SONAR_POSTGRE  
>User: SONAR_POSTGRE  
>Pass: docker123

## 1. **Configurando Sonar Qube;**
### 1. **Acessando;**

*User:* admin;  
*Pass:* admin;  

### 3. **Atualizando Plugins;**

> Administration > Marketplace > Updates Only

Ataulize todos os Plugins

## 3. **Instalando Sonar Scanner;**

Para instalar Sonar Scanner utilize o tutorial abaixo:

[Sonar Scanner](https://docs.sonarqube.org/display/SCAN)

## 4. **Exec;**

```console
sonar-scanner
```

## 5. **Links importantes;**

[TUTORIAL DE MARKDOWN](https://www.markdownguide.org/basic-syntax/)

[Tutorial Docker-Compose](https://docs.docker.com/v17.09/compose/compose-file/#environment)

[Sonar Qube](https://hub.docker.com/_/sonarqube)
[Exemplo Sonar Qube](https://github.com/SonarSource/docker-sonarqube/blob/master/recipes/docker-compose-postgres-example.yml)

[Sonar Scanner](https://hub.docker.com/r/skilldlabs/sonar-scanner)