# Shadow Node Maintenance

More to this section coming soon. 

Join Discord - Shadow Ops channel - https://discord.gg/c7ts863T

# Frequently Asked Questions

1. How do I know if my node is working properly?
2. I ran the Healthcheck curl but received a connection error.
3. Why does the `solana catchup` command return a different slot position than what the Shadow Protocol bot indicates?
4. My node seems to fall off the tip routinely - is this normal or is something wrong?



Healthcheck
```
curl http://localhost:8899 -k -X POST -H "Content-Type: application/json" -d '
  {"jsonrpc":"2.0","id":1, "method":"getHealth"}
'
```

Tracking root slot
```
timeout 120 solana catchup --our-localhost=8899 --log --follow --commitment root
```

curl for getBlockProduction
```
curl http://localhost:8899 -k -X POST -H "Content-Type: application/json" -H "Referer: GGLabs" -d '{"jsonrpc":"2.0","id":1, "method":"getBlockProduction"}
'
```

Grafana Dashboard coming soon


Alerts coming soon.


Useful server commands for running system checks coming soon.


