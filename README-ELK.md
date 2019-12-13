# DPF-Plugins

Modified for headless plugin build for [Elk Audio OS](https://elk.audio)

## Building Instructions

1. Set up the cross-compilation toolchain with:  

   ```bash
   $ unset LD_LIBRARY_PATH
   $ source /path/to/environment-setup-cortexa7t2hf-neon-vfpv4-elk-linux-gnueabi
   ```

2. (optional) Add flags for more aggressive optimizations than the default ones from the toolchain with:  

   ```bash
   $ export CXXFLAGS="-O3 -pipe -ffast-math -felimnate-unused-debug-types -funroll-loops -mvectorize-with-neon-quad"
   ```

3. Finally cross compile the plugin using:  

   ```bash
   $ make plugins
   ```

## Additional notes

* Only the vst plugins have been tried on the Elk Pi.
* For further compilation help. Look at our [documentation](https://github.com/elk-audio/elk-docs/blob/master/documents/building_plugins_for_elk.md).