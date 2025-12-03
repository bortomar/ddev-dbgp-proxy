[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/bortomar/ddev-dbgp-proxy/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/bortomar/ddev-dbgp-proxy/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/bortomar/ddev-dbgp-proxy)](https://github.com/bortomar/ddev-dbgp-proxy/commits)
[![release](https://img.shields.io/github/v/release/bortomar/ddev-dbgp-proxy)](https://github.com/bortomar/ddev-dbgp-proxy/releases/latest)

# DDEV Dbgp Proxy

## Overview

This add-on integrates Dbgp Proxy into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get bortomar/ddev-dbgp-proxy
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Dbgp Proxy |
| `ddev logs -s dbgp-proxy` | Check Dbgp Proxy logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.dbgp-proxy --dbgp-proxy-docker-image="ddev/ddev-utilities:latest"
ddev add-on get bortomar/ddev-dbgp-proxy
ddev restart
```

Make sure to commit the `.ddev/.env.dbgp-proxy` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `DBGP_PROXY_DOCKER_IMAGE` | `--dbgp-proxy-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@bortomar](https://github.com/bortomar)**
