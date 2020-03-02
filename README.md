# Rpi-Wasmer
Try to run wasmer in Raspberry Pi 4
You cannot simply run `curl https://get.wasmer.io -sSfL | sh` in your raspberry pi terminal to install wasmer.
By default, it is not support ARM, even it is already ARM 64

I spend about one day to have wasmer running in my pi. 

1. Install Manjaro ARM 64 to Raspberry Pi. I believe other 64 version of OS for Pi should work, just did not try all of them.
2. Build Wasmer locally on Pi.

There are a few hiccups during the installation, but nothing big. Just in case you got the similar experiences.
1. If you are burnning OS image to micro SD card on a newer MacOS, please run BalenaEtcher using sudo. If you use DD to turn, that's fine. `sudo /Applications/balenaEtcher.app/Contents/MacOS/balenaEtcher  `. If you do not run in sudo, Etcher may give you confusing error message.
2. Bulding wasmer on pi is simple, just follow the instruction https://docs.wasmer.io/ecosystem/wasmer/building-from-source . Make sure you installed those dev tools and dependencies. Manjaro is not using apt apt-get, it uses pacman. 
3. I tried singlepass only. LLVM and Cranelift still not working
4. Rust building is slow, be patient

