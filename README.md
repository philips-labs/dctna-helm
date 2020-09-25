# DCTNA Helm Chart

<!-- This README.md is generated. -->

This repository contains the Helm Chart for installing and configuring [DCTNA](https://github.com/philips-labs/dct-notary-admin) (Docker Content Trust Notary Admin).

![Version: 0.2.2](https://img.shields.io/badge/Version-0.2.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.3](https://img.shields.io/badge/AppVersion-0.1.3-informational?style=flat-square)

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

Kubernetes: `>=1.15.0-0`

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
| server.notary.auth.enabled | bool | `true` |  |
| server.notary.auth.password | string | `""` |  |
| server.notary.auth.username | string | `""` |  |
| server.notary.config.remote_server.skipTLSVerify | bool | `false` |  |
| server.notary.config.remote_server.url | string | `"https://notary.docker.io"` |  |
| server.notary.config.trust_dir | string | `"./data"` |  |
| server.podAnnotations | object | `{}` |  |
| server.podSecurityContext | object | `{}` |  |
| server.resources | object | `{}` |  |
| server.securityContext | object | `{}` |  |
| server.service.httpPort | int | `80` |  |
| server.service.httpsPort | int | `443` |  |
| server.service.name | string | `"https"` |  |
| server.service.type | string | `"ClusterIP"` |  |
| server.terminationGracePeriodSeconds | int | `10` |  |
| server.tolerations | list | `[]` |  |
| server.vault.address | string | `"https://vault.hashicorp-vault:8200"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| web.affinity | object | `{}` |  |
| web.autoscaling.enabled | bool | `true` |  |
| web.autoscaling.maxReplicas | int | `5` |  |
| web.autoscaling.minReplicas | int | `1` |  |
| web.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| web.autoscaling.targetMemoryUtilizationPercentage | int | `80` |  |
| web.image.pullPolicy | string | `"IfNotPresent"` |  |
| web.image.repository | string | `"philipssoftware/dctna-web"` |  |
| web.image.tag | string | `""` |  |
| web.ingress.annotations | object | `{}` |  |
| web.ingress.enabled | bool | `false` |  |
| web.ingress.hosts | object | `{}` |  |
| web.livenessProbe.enabled | bool | `true` |  |
| web.nodeSelector | object | `{}` |  |
| web.podAnnotations | object | `{}` |  |
| web.podSecurityContext | object | `{}` |  |
| web.readinessProbe.enabled | bool | `true` |  |
| web.replicaCount | int | `1` |  |
| web.resources | object | `{}` |  |
| web.securityContext | object | `{}` |  |
| web.service.port | int | `80` |  |
| web.service.type | string | `"ClusterIP"` |  |
| web.tolerations | list | `[]` |  |
