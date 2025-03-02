# streetmerchant
Personal/example repo for deploying [streetmerchant](https://github.com/jef/streetmerchant)

## Configuration
1. Create a file at `inventory/group_vars/overrides.yml` (make sure the first line is `---`)
1. Set new values for any variables defined in `inventory/config.yml`

## Install prerequisets
`ansible-galaxy install -r requirements.yml`

## Deploy container
`ansible-playbook install.yml`

## Test notifications
```
docker compose exec streetmerchant /bin/sh
npm run test:notification:production
```
