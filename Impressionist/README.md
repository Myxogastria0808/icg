# Impressionist

## Build

After cloning this repository and setting up the submodules, type the following.

```sh
mkdir build
cd build
cmake ..
cmake --build .
```

### for Mac

```sh
brew install --cask cmake
mkdir build
cd build
cmake .. -DCMAKE_POLICY_VERSION_MINIMUM=3.5
cmake --build .
```


Then `Impressionist` is created under the `build/` directory.
To run it, type `./Impressionist`.
