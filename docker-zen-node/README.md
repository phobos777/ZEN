# ZEN Securenode: uses Unbuntu 16.04, Docker, Acme Cert and auto renew, Domain DNS

```
git clone https://github.com/phobos777/docker-zen-node && cd docker-zen-node
./install.sh stakeaddr email fqdn region
```

## Put 42 ZEN in each Transparent Address 
## Setup VPS' at provider
## Setup A names at GoDaddy for each VPS
## Run script:

`./install.sh ztjcr2DSYhM44gZ3WFFeoK2hDxhmK4VP3QcgK email@example.com zennode.example.com na` 

## Send 1 ZEN to Private address on node
## Check private balance:

```
docker exec zen-node gosu user zen-cli z_gettotalbalance
``` 

## VPS to fully update to the latest block.status:

```
docker exec zen-node gosu user zen-cli getinfo
```