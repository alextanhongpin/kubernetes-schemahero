# SchemaHero

## Installation


Follow the guide [here](https://schemahero.io/docs/installing/kubectl/).


```bash
$ alias k=kubectl
$ k schemahero version
SchemaHero v0.12.3

# Install.
$ k schemahero install

# Validate.
$ k get po -n schemahero-system

$ k apply -f config
$ k get Database
$ k get databases # Alias
$ k describe Database

# https://schemahero.io/learn/tutorial/create-table/
$ k create ns schemahero-tutorial
$ k apply -f config
$ k get Table -n schemahero-tutorial
$ k get tables -n schemahero-tutorial
$ k schemahero get migrations -n schemahero-tutorial
$ k schemahero describe migration ef096f -n schemahero-tutorial
$ k schemahero -n schemahero-tutorial approve migration ef096f


# To debug Postgres connection.
$ k get po -n schemahero-tutorial
$ k logs test-controller-0 -n schemahero-tutorial

# To debug schemahero system
$ k get po -n schemahero-system
$ k logs schemahero-0 -n schemahero-system
```
