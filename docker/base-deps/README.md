## About
This is an internal image, the [`rayproject/ray`](https://hub.docker.com/repository/docker/rayproject/ray) or [`rayproject/ray-ml`](https://hub.docker.com/repository/docker/rayproject/ray-ml) should be used!


This image  has the system-level dependencies for `Ray` and the `Ray Autoscaler`. The `ray-deps` image is built on top of this. This image is built periodically or when dependencies are added. [Find the Dockerfile here.](https://github.com/ray-project/ray/blob/master/docker/base-deps/Dockerfile)

## Tags

Images are `tagged` with the format `{Ray version}[-{Python version}][-{Platform}][-{Architecture}]`. `Ray version` tag can be one of the following:

| Ray version tag | Description |
| --------------- | ----------- |
| `latest`                     | The most recent Ray release. |
| `x.y.z`                      | A specific Ray release, e.g. 1.12.1 |
| `nightly`                    | The most recent Ray development build (a recent commit from Github `master`) |
| `6 character Git SHA prefix` | A specific development build (uses a SHA from the Github `master`, e.g. `8960af`). |

The optional `Python version` tag specifies the Python version in the image. All Python versions supported by Ray are available, e.g. `py37`, `py38`, `py39` and `py310`. If unspecified, the tag points to an image using `Python 3.7`.

The optional `Platform` tag specifies the platform where the image is intended for:

| Platform tag | Description |
| --------------- | ----------- |
| `-cpu`  | These are based off of an Ubuntu image. |
| `-cuXX` | These are based off of an NVIDIA CUDA image with the specified CUDA version `xx`. They require the Nvidia Docker Runtime. |
| `-gpu`  | Aliases to a specific `-cuXX` tagged image. |
| no tag  | Aliases to `-cpu` tagged images for `ray`, and aliases to ``-gpu`` tagged images for `ray-ml`. |

The optional `Architecture` tag can be used to specify images for different CPU architectures.
Currently, we support the `x86_64` (`amd64`) and `aarch64` (`arm64`) architectures.

Please note that suffixes are only used to specify `aarch64` images. No suffix means
`x86_64`/`amd64`-compatible images.

| Platform tag | Description             |
|--------------|-------------------------|
| `-aarch64`   | arm64-compatible images |
| no tag       | Defaults to `amd64`     |


## Other Images
* [`rayproject/ray`](https://hub.docker.com/repository/docker/rayproject/ray) - Ray and all of its dependencies.
* [`rayproject/ray-ml`](https://hub.docker.com/repository/docker/rayproject/ray-ml) - This image with common ML libraries to make development & deployment more smooth!
<br></br><br></br>

* [`rayproject/ray-deps`](https://hub.docker.com/repository/docker/rayproject/ray-deps) - Internal image with python-level dependencies. 
