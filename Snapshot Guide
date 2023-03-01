# How To Process nolus-rila Snapshot

## Download the snapshot

```
wget -O nolus-rila.tar http://95.217.195.232/nolus-rila.tar --inet4-only
```

## Stop service

```
# Cosmovisor
sudo systemctl stop cosmovisor
```

## Reset data

```
# On some tendermint chains
kujirad unsafe-reset-all

# On other tendermint chains
kujirad tendermint unsafe-reset-all --home $HOME/.kujira --keep-addr-book
```

## Load new data

```
tar -x -C $HOME/.nolus
```

## Start service

```
# Cosmovisor
sudo systemctl start cosmovisor
```

## Check status
```
nolusd status

sudo journalctl -u cosmovisor -f
```
