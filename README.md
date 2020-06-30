# Docker image for Magento 2.x
```bash
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition magento
```

## Set permissions
```bash
cd magento

find . -type d -exec chmod 770 {} + && find . -type f -exec chmod 660 {} + && chmod u+x bin/magento
```
## Docker installation script
git clone https://github.com/rsurfings/magento magento-docker

cd magento-docker docker-compose up -d

## Docker access via bash
```bash
docker exec -it web bash

## Magento install
bin/magento setup:install --backend-frontname=admin --db-host=mysql --db-name=magento --db-user=root --db-password=root --base-url=http://local.domain.com --language=pt_BR --timezone=America/Sao_Paulo --currency=BRL --use-rewrites=1 --use-secure=1 --base-url-secure=https://local.domain.com --admin-user=user --admin-password=senha123 --use-sample-data --admin-firstname=User --admin-lastname=Lastname --admin-email=rsurfings@gmail.com
```
