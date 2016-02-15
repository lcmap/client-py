# lcmap-client-py

LCMAP REST Service Client for Python

[Very WIP ... not ready for use]


## Configuration

Client library configuration is done using a Config/INI file. See the


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

```bash
$  lcmap-client rod --x -1789425 --y 3073665 --t1 2010-01-01 --t2 2015-01-01
```

## Development

$
$


## License

TBD
