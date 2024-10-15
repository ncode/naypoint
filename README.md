----------------------------------------

# Naypoint

* Naypoint is a fork of hashicorp waypoint before the license change

Naypoint allows developers to define their application build, deploy, and release lifecycle as code, reducing the time to deliver deployments through a consistent and repeatable workflow.

Naypoint supports a number of build methods and target platforms out of the box
and more can be easily added via plugins:

* Cloud Native Buildpacks
* Docker
* Kubernetes
* Nomad

Naypoint runs on Linux, Mac OS X, and Windows.

### Running the unit tests

To run the entire test suite, you'll want to ensure that you've brought up
all the required containers used for testing. You can do this by leveraging
the existing `docker-compose.yml` file that's in the root directory of this
project:

```
$ docker-compose up
```

After running this, you should have a local Horizon container along with a few
other services needed for running the tests:

```
$ make test
```

#### Running individual tests

If you don't want to run the entire test suite, you can just run a singe test
with go. For example, if you wanted to run the tests ListInstances, you would
run:

```
$ go test -run ListInstances -v ./internal/server/singleprocess
```
