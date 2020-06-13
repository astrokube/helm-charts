# Minecraft

[Minecraft](https://minecraft.net/) is a game about build and explore.

## Minecraft parameters

| Parameter                   | Description                                                             | Default              |
| --                          | --                                                                      | --                   |
| `server.eula`               | Accept the Mojang EULA                                                  | `false`              |
| `server.bukkitDownloadUrl`  | URL used to download Bukkit JAR                                         | `""`                 |
| `server.paperDownloadUrl`   | URL used to download Paper JAR                                          | `""`                 |
| `server.spigotDownloadUrl`  | URL used to download Spigot JAR                                         | `""`                 |
| `server.type`               | Server type (VANILLA, SPIGOT, BUKKIT, PAPER, FORGE, FTB, SPONGEVANILLA) | `VANILLA`            |
| `server.version`            | Server version                                                          | `1.15.2`             |
| `server.difficulty`         | Server difficulty (peaceful, easy, normal, and hard)                    | `easy`               |
| `server.gameMode`           | Game mode (creative, survival, adventure, spectator)                    | `survival`           |
| `server.generateStructures` | Enable the structures generation                                        | `true`               |
| `server.maxPlayers`         | Set the max players the server can handle                               | `20`                 |
| `server.motd`               | Set the motd used by the server                                         | `A Minecraft Server` |
| `server.onlineMode`         | Enable the check accounts against Minecraft account service             | `true`               |
| `server.ops`                | List of players to set as OP                                            | `""`                 |
| `server.spawnAnimals`       | Enable the animals spawn                                                | `true`               |
| `server.spawnMonsters`      | Enable the monsters spawn                                               | `true`               |
| `server.spawnNPCs`          | Enable the NPCs spawn                                                   | `true`               |
| `server.viewDistance`       | Set the distance view                                                   | `10`                 |

## Minecraft deployment parameters

| Parameter                   | Description                                         | Default                               |
| --                          | --                                                  | --                                    |
| `image.repository`          | Minecraft image repository                          | `itzg/minecraft-server`               |
| `image.pullPolicy`          | Minecraft image pull policy                         | `IfNotPresent`                        |
| `image.tag`                 | Minecraft image tag                                 | `latest`                              |
| `imagePullSecrets`          | Minecraft and SFTP image pull secrets               | `[]`                                  |
| `service.annotations`       | Minecraft service annotations                       | `{                                 }` |
| `service.type`              | Minecraft service type                              | `ClusterIP`                           |
| `service.port`              | Minectaft service port                              | `25565`                               |
| `resources.requests`        | Requested resources for Minecraft                   | `{"cpu":"100m", "memory":"512Mi"   }` |
| `resources.limits`          | The resources limits for Minecraft                  | `{                                 }` |
| `resources.requests`        | The requested resources for the WordPress container | `{"memory": "512Mi", "cpu": "300m" }` |
| `nodeSelector`              | Node labels for pod assignment                      | `{                                 }` |
| `tolerations`               | Tolerations for pod assignment                      | `[]`                                  |
| `affinity`                  | Affinity for pod assignment                         | `{                                 }` |
| `persistence.enabled`       | Enable persistence using PVC                        | `false`                               |
| `persistence.existingClaim` | Enable persistence using an existing PVC            | `nil`                                 |
| `persistence.storageClass`  | PVC Storage Class                                   | `nil`                                 |
| `persistence.accessMode`    | PVC Access Mode                                     | `ReadWriteOnce`                       |
| `persistence.size`          | PVC Storage Request                                 | `1Gi`                                 |
