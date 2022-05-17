### FluentBit metrics demo

Demo for using FluentBit to export metrics using FluentBit. We instrument the application using OpenTelemetry and send the metrics to FluentBit using the OpenTelemetry input plugin, which are then exported using the [Prometheus remote write](https://docs.fluentbit.io/manual/pipeline/outputs/prometheus-remote-write) output plugin. This can be now visualized in Grafana.

### Steps to set up:

1. Clone the repo and navigate to the directory

2. Run `docker-compose up --build`

3. Go to `localhost:3000` and login to Grafana using credentials admin, admin

4. in configuration>data sources select Prometheus and add the url as `http://fluentbit:2021/`

5. Create dashboard to visualize data
