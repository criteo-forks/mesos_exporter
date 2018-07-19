# Build instructions for Criteo

GOOS=linux GOARCH=amd64 go build && name="mesos_exporter-$(git describe --tags --abbrev=0).linux-amd64" && rm -rf $name && mkdir -p $name && cp mesos_exporter LICENSE $name && tar czvf $name.tar.gz $name
