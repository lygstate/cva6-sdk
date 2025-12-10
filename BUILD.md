# Building for qemu


## Building the container
```bash
pushd container
docker build -t ghcr.io/pulp-platform/ariane-sdk -f Dockerfile .
popd
```

## Build the image
```
git submodule update --init --recursive
docker run --rm -it -v `pwd`:/repo -w /repo -u $(id -u ${USER}):$(id -g ${USER}) ghcr.io/pulp-platform/ariane-sdk
make images

```
