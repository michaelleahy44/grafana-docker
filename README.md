# Grafana Docker Setup

Clone the repo:
```bash
git clone https://github.com/michaelleahy44/grafana-docker
```

## Grafana Server
1. Navigate to the server directory
    ```bash
    cd grafana-docker/grafana-server
    ```

2. Replace `<SERVER_IP>` with the IP address of the machine in the `grafana.ini`file

3. Change permissions of the `loki-data` directory
    ```bash
    sudo sudo chown -R 10001:10001 loki-data
    ```

4. Edit `<CLIENT_IP>` with the IP of the client machines in the `prometheus.yml` file

5. Bring the containers up
    ```bash
    docker compose up -d
    ```

## Grafana Client
1. Navigate to the client directory
    ```bash
    cd grafana-docker/grafana-client
    ```

2. Replace `<SERVER_IP>` with the IP address of the server machine in the `promtail.yml`file. Replace `<MACHINE_NAME>` with the name of the machine in the `promtail.yml` file

3. Bring the containers up
    ```bash
    docker compose up -d
    ```
