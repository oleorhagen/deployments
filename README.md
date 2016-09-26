# Deployments
[![Build Status](https://travis-ci.com/mendersoftware/deployments.svg?token=rx8YqsZ2ZyaopcMPmDmo&branch=master)](https://travis-ci.com/mendersoftware/deployments)
[![Coverage Status](https://coveralls.io/repos/github/mendersoftware/deployments/badge.svg?branch=master&t=n7mVVE)](https://coveralls.io/github/mendersoftware/deployments?branch=master)

Mender: Deployments Service
==============================================

Mender is an open source over-the-air (OTA) software updater for embedded Linux
devices. Mender comprises a client running at the embedded device, as well as
a server that manages deployments across many devices.

This repository contains the Mender Deployments service, which is part of the
Mender server. The Mender server is designed as a microservices architecture
and comprises several repositories.

Deployments Service is the central module concerned with the management of software artifacts and updates. It allows
the user to define and schedule deployments for selected groups of devices, and dispatches them accordingly - all
the while monitoring the status and progress of installations.


![Mender logo](https://mender.io/user/pages/04.resources/_logos/logoS.png)


## Getting started

To start using Mender, we recommend that you begin with the Getting started
section in [the Mender documentation](https://docs.mender.io/).


## Building from source

As the Mender server is designed as microservices architecture, it requires several
repositories to be built to be fully functional. If you are testing the Mender server it
is therefore easier to follow the getting started section above as it integrates these
services.

If you would like to build the Deployments Service independently, you can follow
these steps:

```
git clone https://github.com/mendersoftware/deployments.git
cd deployments
go build
```

## Configuration

The service is configured by providing configuration file (supports JSON, TOML, YAML and HCL formatting).
The default configuration file is provided to be downloaded from [config.yaml](https://github.com/mendersoftware/deployments/blob/master/config.yaml).

Application requirements:
* Access to AWS S3 bucket, keys can be configured in several ways, documented in the configuration file.
* Access to MongoDB instance and configured in config file. [Installation instructions](https://www.mongodb.org/downloads#)
* Access to Mender Gateway with Integration API access.

## Contributing

We welcome and ask for your contribution. If you would like to contribute to Mender, please read our guide on how to best get started [contributing code or
documentation](https://github.com/mendersoftware/mender/blob/master/CONTRIBUTING.md).

## License

Mender is licensed under the Apache License, Version 2.0. See
[LICENSE](https://github.com/mendersoftware/deployments/blob/master/LICENSE) for the
full license text.

## Security disclosure

We take security very seriously. If you come across any issue regarding
security, please disclose the information by sending an email to
[security@mender.io](security@mender.io). Please do not create a new public
issue. We thank you in advance for your cooperation.

## Connect with us

* Join our [Google
  group](https://groups.google.com/a/lists.mender.io/forum/#!forum/mender)
* Follow us on [Twitter](https://twitter.com/mender_io?target=_blank). Please
  feel free to tweet us questions.
* Fork us on [Github](https://github.com/mendersoftware)
* Email us at [contact@mender.io](mailto:contact@mender.io)
