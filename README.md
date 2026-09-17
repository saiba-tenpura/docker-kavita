# Docker Kavita
My personal Kavita docker compose setup incl. an external Traefik instance for serving the web interface.

## Configuring OIDC
In order to to configure OIDC you first need an identity provider (IdP) in this example Authentik is used because it can also be setup via my other [repository](https://github.com/saiba-tenpura/docker-authentik).

```
# config/appsettings.json
{
  ....,
  "OpenIdConnectSettings": {
    "Authority": "https://authentik.example.com/application/o/kavita/",
    "ClientId": "<OIDC_CLIENT_ID>",
    "Secret": "<OIDC_CLIENT_SECRET>",
    "CustomScopes": [],
    "Enabled": true
  }
}
```

## License
[MIT](./LICENSE)
