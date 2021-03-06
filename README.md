# elastic-sandbox
Scripts for setting up Elastic Stack environments for sandbox purposes

# Starting Elastic core services

## Single-node Elasticsearch setup

`cd single`
`docker-compose up`

# Services

The ElasticSearch API will be exposed at: [http://localhost:9200](http://localhost:9200)

The Kibana API will be exposed at [http://localhost:5601](http://localhost:5601)

# PacketBeat

Assuming you're running on a Mac _and_ would like to capture traffic on your host machine, do not run PacketBeat in a Docker container.  Docker for Mac does not support host networking, which would be required for the container to capture the Mac's traffic.

Instead, download PacketBeat for Mac separately and run with the supplied configuration file:

`cd packetbeat`
`sudo ./packetbeat -c <path-to-packetbeat.yml>`

PacketBeat will generate Kibana dashboards where the captured network traffic will be visible.
