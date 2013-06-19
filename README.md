VCAP Metric Collector
=====================
The `collector` will discover the various components on the message bus and
query their /healthz and /varz interfaces.

The metric data collected is published to collector plugins. See the `lib/historian` folder for [available plugins](https://github.com/cloudfoundry/collector/tree/master/lib/collector/historian) such as OpenTSDB, AWS CloudWatch and DataDog. Plugins are extensible to publish data to other systems.

Additional metrics can be written by providing
`Handler` plugins. See `lib/collector/handler.rb` and
`lib/collector/handlers/dea.rb` for an example.
