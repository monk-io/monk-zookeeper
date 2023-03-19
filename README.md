# Zookeeper & Monk

This repository contains Monk.io template to deploy Zookeeper either locally or on cloud of your choice (AWS, GCP, Azure, Digital Ocean).

## Prerequisites

- [Install Monk](https://docs.monk.io/docs/get-monk)
- [Register and Login Monk](https://docs.monk.io/docs/acc-and-auth)
- [Add Cloud Provider](https://docs.monk.io/docs/cloud-provider)
- [Add Instance](https://docs.monk.io/docs/multi-cloud)

## Make sure monkd is running

```bash
foo@bar:~$ monk status
daemon: ready
auth: logged in
not connected to cluster
```

## Clone Repository

```bash
git clone https://github.com/monk-io/monk-zookeeper
```

## Load Template

```bash
cd monk-zookeeper
monk load MANIFEST
```

## Let's take a look at the themes I have installed

```bash
foo@bar:~$ monk list zookeeper
✔ Got the list
Type      Template  Repository  Version  Tags
runnable  zookeeper/monk-zookeeper  local       -        -
```

## Deploy Stack

```bash
foo@bar:~$ monk run zookeeper/monk-zookeeper
```

## Variables

| Variable     | Description                   | Default |
|--------------|-------------------------------|---------|
| port         | Zookeeper port                | 2181    |
| image        | Docker image tag              | latest  |
| admin_server | Zookeeper admin server enable | true    |

## Stop, remove and clean up workloads and templates

```bash
monk purge -a
```
