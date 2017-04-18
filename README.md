# nmap Autodiscovery for Automatron

This is a simple nmap based Autodiscovery plugin for Automatron

## Install instructions


Place `nmap` directory to the Automatron `plugins/discovery/` directory.

```shell
$ cp -R nmap /path/to/plugins/discovery/
```

Install Python dependencies with `pip`.

```shell
$ pip install -r requirements.txt
```

Add configuration to Automatron `config/config.yml` file.

```yaml
discovery:
  plugins:
    nmap:
      target: 10.0.0.1/8
      flags: -sP
      interval: 40
```

The above configuration has three main elements.

* `target` - This is the target to pass on to `nmap`.

The value of `10.0.0.1/8` will scan the entire `10.0.0.0` class A network.

* `flags` - These are flags you would pass to `nmap` when run from command line.

The value of `-sP` will perform a Ping based scan.

* `interval` - The specified "interval" (in seconds) to wait before performing another scan.
