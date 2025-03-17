# helm-values

This repository contains Helm values for various public charts from Bitnami.

## Adding Bitnami Repository

To add the Bitnami repository to Helm, use the following commands:

```sh
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
```

## Installing and Upgrading Charts

### PostgreSQL

To install the PostgreSQL chart:

```sh
helm install postgresql bitnami/postgresql
```

To upgrade the PostgreSQL chart with custom values:

```sh
helm upgrade postgresql bitnami/postgresql -f postgresql/values.yaml
```

### MariaDB

To install the MariaDB chart:

```sh
helm install mariadb bitnami/mariadb
```

To upgrade the MariaDB chart with custom values:

```sh
helm upgrade mariadb bitnami/mariadb -f mariadb/values.yaml
```

To upgrade the MariaDB chart with replication values:

```sh
helm upgrade mariadb bitnami/mariadb -f mariadb/values-replication.yaml
```

## Directory Structure

- `mariadb/`
  - `values.yaml`: Values for standalone MariaDB deployment.
  - `values-replication.yaml`: Values for MariaDB deployment with replication.
- `postgresql/`
  - `values.yaml`: Values for PostgreSQL deployment.

## Contributing

Feel free to contribute by submitting a pull request or opening an issue.

## License

This project is licensed under the MIT License.