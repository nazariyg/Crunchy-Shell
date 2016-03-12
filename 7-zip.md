# 7-zip

    sudo apt-get install p7zip p7zip-full
    tar cfv - <srcdir> | 7z a -si -mx=9 -ms=on <dstarchfile>.tar.7z
    tar cfv - <srcdir> | 7z a -si -mx=9 -ms=on -p<password> -mhe=on <dstarchfile>.tar.7z
    7z x -so <srcarchfile>.tar.7z | tar xfv -
    7z x -so -p<password> <srcarchfile>.tar.7z | tar xfv -
    7z a -mx=9 -ms=on <dstarchfile>.7z <srcdir>
    7z a -mx=9 -ms=on -p<password> -mhe=on <dstarchfile>.7z <srcdir>
    7z e <srcarchfile>.7z
    7z e -p<password> <srcarchfile>.7z
    7z t <archfile>.7z
