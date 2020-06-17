# BungeeCord

[BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) is a proxy between the player's client and the connected Minecraft servers.

## BungeeCord parameters

| Parameter                   | Description                                                               | Default          |
| --                          | --                                                                        | --               |
| `server.type`               | Server type (BUNGEECORD, WATERFALL)                                       | `BUNGEECORD`     |
| `server.memory`             | Memory assigned to the JVM                                                | `512m`           |
| `server.jvmOpts`            | Additional -X options to pass to the JVM                                  | `""`             |
| `plugins`                   | Separated list of JAR files that will be downloaded in the plugins folder | `""`             |
| `server.config.motd`        | Server MOTD                                                               | `&1Bugee server` |
| `server.config.onlineMode`  | Enable the check accounts against Minecraft account service               | `true`           |
| `server.config.playerLimit` | Global player limit. 0 or negative values means unlimited                 | `-1`             |
| `server.config.servers`     | List of backend servers to use                                            | `[]`             |
| `server.config.priorities`  | Set the priority on the list of server to join                            | `[]`             |

## BungeeCord deployment parameters

| Parameter                   | Description                              | Default                               |
| --                          | --                                       | --                                    |
| `image.repository`          | BungeeCord image repository              | `pasqualet/bungeecord`                |
| `image.pullPolicy`          | BungeeCord image pull policy             | `IfNotPresent`                        |
| `image.tag`                 | BungeeCord image tag                     | `latest`                              |
| `imagePullSecrets`          | BungeeCord and SFTP image pull secrets   | `[]`                                  |
| `service.annotations`       | BungeeCord service annotations           | `{                                 }` |
| `service.type`              | BungeeCord service type                  | `LoadBalancer`                        |
| `service.port`              | Minectaft service port                   | `25565`                               |
| `resources.requests`        | Requested resources for BungeeCord       | `{"memory":"512Mi"   }`               |
| `resources.limits`          | The resources limits for BungeeCord      | `{                                 }` |
| `nodeSelector`              | Node labels for pod assignment           | `{                                 }` |
| `tolerations`               | Tolerations for pod assignment           | `[]`                                  |
| `affinity`                  | Affinity for pod assignment              | `{                                 }` |
| `persistence.enabled`       | Enable persistence using PVC             | `false`                               |
| `persistence.existingClaim` | Enable persistence using an existing PVC | `nil`                                 |
| `persistence.storageClass`  | PVC Storage Class                        | `nil`                                 |
| `persistence.accessMode`    | PVC Access Mode                          | `ReadWriteOnce`                       |
| `persistence.size`          | PVC Storage Request                      | `1Gi`                                 |
