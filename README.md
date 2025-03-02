# streetmerchant
Personal/example repo for deploying [streetmerchant](https://github.com/jef/streetmerchant)

This playbook assumes you have a docker container named `docker-vpn` running, with which it will share a network stack. [docker-vpn-pia](https://github.com/hobointhecorner/hobo.ansible.docker-vpn-pia) can be used if you subscribe to Private Internet Access.

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
