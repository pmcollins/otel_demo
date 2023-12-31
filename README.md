# OTel Demo

This directory contains several applications that can be used to explore and test the generation of telemetry from
a variety of Python libaries. The libraries which are used by these applications, and supported by OTel, are the
following: DB-API, sqlite3, gRPC, Bottle, Django, Fastapi, Flask, Pyramid, Tornado, Httplib, Requests, and Httpx.

The primary application in this directory is [django](django), which contains a web app as well as
a few commands (see the Django [README.md](django/README.md) for more info). The other
directories ([bottle](bottle), [fastapi](fastapi), [flask](flask), [pyramid](pyramid), and [tornado](tornado)) contain
skeletal applications using the framework specified by the directory name. These applications have a single endpoint
each, which are called by the Django web app upon user request.

### Operation

To start all services, run `./start.sh`. This will cause seven services to start: `django/ingest`, `fastapi`, `flask`,
`bottle`, `pyramid`, `tornado`, and `django/runserver`. By default, these sevices send telemetry message to the
local backend, which by default are intercepted and handled by `django/ingest`.
