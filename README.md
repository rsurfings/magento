# Docker image for Magento 2.x
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition magento

git clone https://github.com/rsurfings/magento magento-docker

## Docker installation script
cd magento-docker docker-compose up -d

```bash
docker exec -it web bash

bin/magento setup:install --backend-frontname=admin --db-host=mysql --db-name=magento --db-user=root --db-password=root --base-url=http://local.domain.com --language=pt_BR --timezone=America/Sao_Paulo --currency=BRL --use-rewrites=1 --use-secure=1 --base-url-secure=https://local.domain.com --admin-user=user --admin-password=senha123 --use-sample-data --admin-firstname=User --admin-lastname=Lastname --admin-email=rsurfings@gmail.com
```
