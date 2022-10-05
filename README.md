[Contribute via OpenShift Dev Spaces](https://devspaces.apps.ocp.ocp-gm.de/#https://github.com/sa-mw-dach/octo-happiness-template-java?che-editor=eclipse/che-theia/latest)

# octo-happiness-template-java# octo-happiness-template-java Project

This project shows an easy to use and full install of an application pipeline and deployment via helm.

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```bash
./mvnw compile quarkus:dev
```

or via quarkus cli, just run 
```bash
quarkus dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

1. Login to your oc cli
1. Navigate to the infra/helm folder and run
1. ```helm upgrade -i octo-happiness-template-java .```

## Uninstall

You can uninstall the installed helm chart via
```bash
helm uninstall octo-happiness-template-java 
```

Afterwards you will have do delete the pvc manually 
```bash
oc delete pvc builder-pvc-2
```