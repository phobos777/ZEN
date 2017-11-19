# 1) Unbuntu 16.04, 2) Docker 3) acme cert and auto renew 4) Domain and nodes.  

```
git clone https://github.com/phobos777/docker-zen-node
./install.sh stakeaddr email fqdn region
```

- Stakeaddr is the transparent address which has your 42 ZEN
- Email is your notification email address should your node have issues
- FQDN is the hostname which must point to the IP address of your server
- Region must either be eu, na or sea

Example:

`./install.sh ztjcr2DSYhMZZ3WFFeoK2hDxhmK4VP3QcgK email@example.com zennode.example.com na`

The script will install the required dependencies and deploy the three containers on your host.

acme.sh is used to provision and maintain a valid SSL certificate on your domain.

The script should execute successfully when you see the output similar to this:

```
## Generating shield address for node...

ztSpgr2Yat7zSMiLNHtyDKGajzSesxabQsRwJnqtomDJU9wd6LzZppnQJyYiNE8sJDEy5MyTiMrSjf3bWcMKgtF9xcEY4eA
```

This will be the shield address you need to send 1 ZEN in order for your start accepting challenges.

After you send your 1 ZEN, you may check your node private balance:

```
docker exec zen-node gosu user zen-cli z_gettotalbalance
```

*Please Note:* It may take up to 1-2 hours for your VPS to fully update to the latest block.

You may check the latest block status with the following command:

```
docker exec zen-node gosu user zen-cli getinfo
```

## Troubleshooting

If you need to execute commands with `zen-cli` you will need to append the following:

```
docker exec zen-node gosu user zen-cli
```

