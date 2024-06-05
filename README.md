# Bevy Template
A template I made to doesn't have to re-create the same setup each time I use bevy

# Setup
in `.cargo/config.toml` You need to change the path of the LLD Linker of your target in :
```toml
rustflags = [
  "-Clink-arg=-fuse-ld=<insert your path here>", # Use LLD Linker
  "-Zshare-generics=y",                                   # (Nightly) Make the current crate share its generic instantiations
  "-Zthreads=0",                                          # (Nightly) Use improved multithreading with the recommended amount of threads.
]
```
