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

# The following line should be executed for the very clean build or the first time build
rm -rf buildroot/output*
mkdir -p buildroot/output-cache

docker run --rm -it -v $PWD/buildroot/output-cache:/home/lygstate/.cache -v `pwd`:/repo -w /repo -u $(id -u ${USER}):$(id -g ${USER}) ghcr.io/pulp-platform/ariane-sdk

docker run --rm -it -v $PWD/buildroot/output-cache:/home/lygstate/.cache -v `pwd`:/repo -w /repo ghcr.io/pulp-platform/ariane-sdk

make images

```

## Building vitetris

```
rm rootfs/tetris
make rootfs/tetris
```
