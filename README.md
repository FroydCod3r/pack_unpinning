# pack_unpinning
Coletânea de Scripts para SSL Pinning em apps Android
Foi adicionado um script para bypass em mecanismos Anti-Root

# poc with frida-client
frida --codeshare script.js -U -f <package_name> --no-pause

frida -U -f <package_name> -l script.js --no-pause

# poc with frida-inject
./frida-inject-14.2.18-android-x86_64 -p $(pidof <package_name>) -s scripts/unpinning.js -e

# poc inject multiples scripts with frida-inject on runtime
$ for f in $(ls /data/local/tmp/scripts/*js); do ./frida-inject-14.2.18-android-x86_64 -p $(pidof <package_name>) -s $f -e; done

É possível capturar o <package_name> usando:
$ frida-ps -U

Ou fazendo o decompile do Android_manifest.xml
