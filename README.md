# pbs-redirector
Small repo to properly redirect domains to other locations

## How to add another redirect

You need to edit the following things:
- the Caddyfile configmap
- the ingress to add the new host

After that, just apply the changes with `kubectl apply -f <file>` and easyiest then delete the caddy pod to reload the config.