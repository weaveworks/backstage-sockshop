# backstage-sockshop

Sockshop Microservice declarations in Backstage.

This is purely for demo purposes.

## Including in a Backstage environment

Update your app-config.local.yaml

First to allow sourcing the API definitions directly from the Sockshop Repo
```yaml
backend:
  reading:
    allow:
    - host: raw.githubusercontent.com
```

And to source the entities from this repository
```yaml
catalog:
  rules:
    - allow: [Component, System, API, Resource, Location, User, Group]
  locations:
    - type: url
      target: https://github.com/weaveworks/backstage-sockshop/blob/main/all.yaml
```
