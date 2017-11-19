# 1) Unbuntu 16.04, 2) Docker 3) acme cert and auto renew 4) Domain and nodes.  

```
git clone https://github.com/phobos777/docker-zen-node && cd docker-zen-node
./install.sh stakeaddr email fqdn region
```

- Stakeaddr is the transparent address which has your 42 ZEN
- Email is your notification email address should your node have issues
- FQDN is the hostname which must point to the IP address of your server
 

Example:

`./install.sh ztjcr2DSYhMZZ3WFFeoK2hDxhmK4VP3QcgK email@example.com zennode.example.com na`

. - send 1 ZEN in order for your start accepting challenges.

After you send your 1 ZEN, you may check your node private balance:

```
docker exec zen-node gosu user zen-cli z_gettotalbalance
```

. - VPS to fully update to the latest block.

You may check the latest block status with the following command:

```
docker exec zen-node gosu user zen-cli getinfo
```

