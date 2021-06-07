# pack_unpinning
Coletânea de Scripts para SSL Pinning em apps Android

# poc with frida-client
frida --codeshare frida_multiple_unpinning.js -U -f <package_name> --no-pause
frida -U -f <package_name> -l frida_multiple_unpinning.js --no-pause
