# Grist Fiddle

This is a testbench to experiment with the behavior of the `grist-oss` docker container. See `.env` and `docker-compose.yml`

This configuration uses a mock OIDC provider, which can be set up locally with `https://github.com/geigerzaehler/oidc-provider-mock`

# Getting Started

To start the app:

```bash
bash scripts/compose
```

To stop the app:

```bash
bash scripts/down
```