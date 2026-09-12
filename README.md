# pbs-redirector
Small tool to properly redirect domains to other locations

## How to add another redirect

Add another entry to the `values.yaml` file:

```yaml

    # unique one word identifier
  - name: example
    # hostnames to listen for
    hostnames:
      - example.scout.ch
      - example.pbs.ch
    # target hostname to redirect to
    target: example.scouts.ch
    # optional: if redirect to a subpath
    path: /optional/example
    # http status code to be used. should be 301 (Moved Permanently) or 302 (Temporary)
    statusCode: 301

```

Additionally, you need to edit the DNS zone and add a `CNAME` entry pointing to `traefik.k8s.tractor.scout.ch`