# RSYNC

    rsync -azv --delete -e ssh <srclocal>/ <dstremoteusername>@<dstremotehost>:<dstremote>
    rsync -azv --delete -e ssh <srcremoteusername>@<srcremotehost>:<srcremote>/ <dstlocal>
    rsync -azv --delete -e 'ssh -i <key> -p <port>' <srclocal>/ <dstremoteusername>@<dstremotehost>:<dstremote>
    rsync -azv --delete -e 'ssh -i <key> -p <port>' <srcremoteusername>@<srcremotehost>:<srcremote>/ <dstlocal>
    rsync -azvn <...>
