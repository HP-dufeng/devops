# devops
use ansible auto install devops infrastructure

# Individual components
- coredns
- gitlab 
- nexus oss
- harbor
- glusterfs
- heketi
- kubernetes
- jenkins

# Heketi
* heketi server must ssh to each node of gluster
* ansible-playbook
* Load a topology file with heketi-cli
    ```
    export HEKETI_CLI_SERVER=http://<heketi server and port>
    heketi-cli --user admin --secret passwrod topology load --json=/var/lib/heketi/topology.json
    ```

