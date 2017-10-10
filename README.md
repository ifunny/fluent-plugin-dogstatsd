# fluent-plugin-dogstatsd

Fluend plugin for Dogstatsd, that is statsd server for Datadog.

## Fork changes

This sections described changes that have been done after fork.

1. Removed options `use_tag_as_key`, `use_tag_as_key_if_missing`, `flat_tags`, `flat_tag`, `value_key`.
4. Appended fluentd event tag parsing to send to Dogstatsd under the tag.
2. Appended option `key_name` to clearly set the statsd metric name. The original plugin supports only `use_tag_as_key` and `value_key` options.
3. Appended option `dogstatsd_tag_name` to name the tag of Dogstatsd metric.

## Installation

    $ gem install specific_install
    $ td-agent-gem specific_install -l https://github.com/ifunny/fluent-plugin-dogstatsd

## Usage

```
<store>
  @type dogstatsd
  metric_type increment
  key_name ifunny.fluentd.messages.rate_avg
  dogstatsd_tag_name log_name
</store>
```

Supported type is only `increment`.

## Contributing

1. Fork it ( https://github.com/ryotarai/fluent-plugin-dogstatsd/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
