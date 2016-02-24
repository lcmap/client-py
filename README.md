# lcmap-client-py

LCMAP REST Service Client for Python

[Very WIP ... not ready for use]


## Configuration

Client library configuration is done using a Config/INI file. For more
information, visit the client documentation link below -- in particular, the
section "The Client Libraries" > "Configuration".


## Documentation

Full documentation for all LCMAP clients is available here:
 * http://usgs-eros.github.io/lcmap-client-docs/current/

Note that per-client usage and example code is selectable via tabs in the upper-right of that page.


## Example Usage

Starting:

```bash
$ cd lcmap-client-py
$ tox -e py34-shell
```

```python
>>> from lcmap_client import Client
>>> client = Client()
>>> result = client.models.samples.os_process.run(year=2017, delay=10)
>>> result.follow_link()
```

## CLI Tools

Run a query:

```bash
$  lcmap query rod --x -1789425 --y 3073665 --t1 2010-01-01 --t2 2015-01-01
```

Execute the same query against the CCDC model:

```bash
$  lcmap model ccdc --x -1789425 --y 3073665 --t1 2010-01-01 --t2 2015-01-01 \
        --row=2241 --col=1231 --out-dir="stdout" --scene-list="stdin"
```

To see what's available:

```bash
$ lcmap --help
```

And for help on the subcommands:

```bash
$ lcmap query --help
$ lcmap query rod --help
```


## Development

TBD


## License

Copyright © 2015 United States Government

NASA Open Source Agreement, Version 1.3.
