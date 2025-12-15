# Deegle Yocto Linux

Deegle Linux provides images for:

- QEMU: `qemu.yml`
- BeagleBone Black: `bbb.yml`
- PocketBeagle 2: `pocketbeagle2.yml`

## Setup the repo

This repoistory makes use of submodules.
You can clone it using `git clone --recurse-submodules <URL>`,
or run  `git submodule update --init --recursive` after cloning.

To build the images, the [kas](https://github.com/siemens/kas) tool is used.
To prepare a virtual Python environment providing `kas` and all other used tool run:

- Prepare a virtual Python environment: `python3 -m venv venv`
- Activate the virtual Python environment: `source venv/bin/activate`
- Install `kas` and other tools: `pip install -r python_packages.txt`

## Build an image

To build and image, do:

- Activate the virtual Python environment: `source venv/bin/activate`
- Run the `kas` build: `kas build <name>.yml`

