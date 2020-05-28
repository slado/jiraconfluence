# Docker s Jira a Confluence
## Struktura
docker-compose obsahuje
- Jira - aktualna verzia
- Confluence - aktualna verzia
- nginx - reverse proxy. Koli tomu, ze vo windows sa neda mountnut priamo subor, ale iba adresar, je nginx potrebne buildnut so spravnou konfiguraciou. Preto je vo foldri nginx dockerfile, do ktoreho sa vlozi aj konfiguracia

> Zapoznamkovany je bitbucket (obdoba GitHubu). Po odpoznamkovani a zmene konfiguracie nginx (kompletna aj s bitbucketom je v nginx.conf.all) je mozne si to vyskusat kompletne

## Adresy
- http://jira.internal
- http://confluence.internal
- http://bitbucket.internal

Do hosts treba pridat
```
127.0.0.1 jira.internal
127.0.0.1 confluence.internal
127.0.0.1 bitbucket.internal
```

## Spustenie
```
docker-compose up -d
```

## Stopnutie
```
docker-compose down
```
