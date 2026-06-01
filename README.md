# AvaFrame Pixi Stable Environment

A minimal [pixi](https://pixi.sh) environment providing QGIS and the latest stable
[AvaFrame](https://github.com/avaframe/AvaFrame) release from PyPI.

This is intended for users who want a ready-to-use AvaFrame + QGIS setup without
installing the full development version from source.

## Prerequisites

Install pixi:

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

Or use your package manager. See the [pixi installation
guide](https://pixi.sh/latest/#installation) for alternatives.

## Getting Started

```bash
git clone https://github.com/avaframe/AvaFramePixiStableEnv.git
cd AvaFramePixiStableEnv
pixi run qgis
```

Install the [OpenNHM QGis
Connector](https://github.com/OpenNHM/OpenNHMQGisConnector) plugin in QGIS
(Plugins > Manage and Install Plugins) to access AvaFrame workflows from the
QGIS interface.

## Environments

| Environment   | Contents                      |
| ------------- | ----------------------------- |
| `default`     | QGIS + latest stable AvaFrame |
| `qgis-stable` | Same as `default` (alias)     |

## Updating

To update to the latest AvaFrame release:

```bash
pixi update
```

## Notes

- `numpy` is pinned to `<2.0` for compatibility with QGIS.
- AvaFrame is installed from PyPI (`avaframe` package), not built from source.
- For the full development setup, see the [AvaFrame
  repository](https://github.com/avaframe/AvaFrame).
