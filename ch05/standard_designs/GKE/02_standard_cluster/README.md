```
                                                +---------+
                                                |End users|
                                                +----+----+
                                                     |
                                                     |
                                      +--------------+--------------+
                                      |Google Cloud Load Balancers  |
                                      |Type:                        |
                                      |Internal HTTPS Load Balancing|
                +---------------------+--------------+--------------+---------------------+
                |                                    |                                    |
+---------------v-----------------+ +----------------v----------------+ +-----------------v---------------+
|      Zone: us-central1-a        | |      Zone: us-central1-b        | |      Zone: us-central1-c        |
| +-----------------------------+ | | +-----------------------------+ | | +-----------------------------+ |
| |  Node pool:                 | | | |  Node pool:                 | | | |  Node pool:                 | |
| |  us-central1-a node         | | | |  us-central1-b node         | | | |  us-central1-c node         | |
| | +-------------------------+ | | | | +-------------------------+ | | | | +-------------------------+ | |
| | |GKE Worker Node a01      | | | | | |GKE Worker Node b01      | | | | | |GKE Worker Node c01      | | |
| | +-------------------------+ | | | | +-------------------------+ | | | | +-------------------------+ | |
| | |Rancher Server pod       | | | | | |Rancher Server pod       | | | | | |Rancher Server pod       | | |
| | |and other related pods   | | | | | |and other related pods   | | | | | |and other related pods   | | |
| | |                         | | | | | |                         | | | | | |                         | | |
| | +-------------------------+ | | | | +-------------------------+ | | | | +-------------------------+ | |
| | |Ingress-Nginx-Controller | | | | | |Ingress-Nginx-Controller | | | | | |Ingress-Nginx-Controller | | |
| | +-------------------------+ | | | | +-------------------------+ | | | | +-------------------------+ | |
| | |Worker                   | | | | | |Worker                   | | | | | |Worker                   | | |
| | +-------------------------+ | | | | +-------------------------+ | | | | +-------------------------+ | |
| |                             | | | |                             | | | |                             | |
| +-----------------------------+ | | +-----------------------------+ | | +-----------------------------+ |
|                                 | |                                 | |                                 |
+---------------------------------+ +---------------------------------+ +---------------------------------+
```