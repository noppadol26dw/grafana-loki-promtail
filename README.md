# Project: Grafana Loki Promtail

## Description
This project provides a comprehensive guide on setting up and using Grafana Loki with Promtail for log aggregation and visualization.

## Features
- Easy installation and configuration of Grafana Loki and Promtail
- Examples of querying and visualizing logs using Grafana

## Getting Started
To get started with this project, follow the instructions below:

1. **Clone the repository to your local machine.**
    ```bash
    git clone https://github.com/noppadol26dw/grafana-loki-promtail.git
    cd grafana-loki-promtail/
    ```

2. **Use Docker Compose to create the services.**
    ```bash
    docker compose up -d
    ```

3. **Access the following services:**
    - **Grafana:** [http://localhost:3000](http://localhost:3000) with the default credentials `admin`/`admin`
    - **Loki:** [http://localhost:3100/ready](http://localhost:3100/ready)

4. **Add Loki data source in Grafana.**
    - Navigate to: `Grafana -> Data Sources -> Add data source -> Loki`
    - Set the **URL** to `http://loki:3100` (Loki's service name defined in `docker-compose.yaml`)
    - Leave other settings as default
    - Click **Save & Test**

5. **Explore the results.**
    - Navigate to: `Grafana -> Explore`
    - Set **Label filter** to `service_name`
    - Set **Value** to `varlogs`
    - Run queries to see the results