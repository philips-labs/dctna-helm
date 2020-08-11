# DCTNA Helm Chart

<!-- This README.md is generated. -->

This repository contains the Helm Chart for installing and configuring [DCTNA](https://github.com/philips-labs/dct-notary-admin).

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A Helm chart for DCTNA.

**Homepage:** <https://github.com/philips-labs/dct-notary-admin>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Marco Franssen | marco.franssen@philips.com |  |

## Source Code

* <https://github.com/philips-labs/dct-notary-admin>
* <https://github.com/philips-labs/dctna-helm>

## Requirements

Kubernetes: `>=1.15`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| fullnameOverride | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` |  |
| server.affinity | object | `{}` |  |
| server.dataStorage.accessMode | string | `"ReadWriteOnce"` |  |
| server.dataStorage.enabled | bool | `true` |  |
| server.dataStorage.size | string | `"1Gi"` |  |
| server.dataStorage.storageClass | string | `nil` |  |
| server.image.pullPolicy | string | `"IfNotPresent"` |  |
| server.image.repository | string | `"philipssoftware/dctna-server"` |  |
| server.image.tag | string | `""` |  |
| server.nodeSelector | object | `{}` |  |
| server.notary.address | string | `"https://notary.docker.io"` |  |
| server.podAnnotations | object | `{}` |  |
| server.podSecurityContext | object | `{}` |  |
| server.resources | object | `{}` |  |
| server.securityContext | object | `{}` |  |
| server.service.name | string | `"https"` |  |
| server.service.port | int | `443` |  |
| server.service.type | string | `"ClusterIP"` |  |
| server.terminationGracePeriodSeconds | int | `10` |  |
| server.tolerations | list | `[]` |  |
| server.vault.address | string | `"https://vault-server.hashicorp-vault"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| web.affinity | object | `{}` |  |
| web.image.pullPolicy | string | `"IfNotPresent"` |  |
| web.image.repository | string | `"philipssoftware/dctna-web"` |  |
| web.image.tag | string | `""` |  |
| web.nodeSelector | object | `{}` |  |
| web.podAnnotations | object | `{}` |  |
| web.podSecurityContext | object | `{}` |  |
| web.replicaCount | int | `1` |  |
| web.resources | object | `{}` |  |
| web.securityContext | object | `{}` |  |
| web.service.port | int | `80` |  |
| web.service.type | string | `"ClusterIP"` |  |
| web.tolerations | list | `[]` |  |
