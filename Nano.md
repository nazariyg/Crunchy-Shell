# Nano

    ['set regexp']                 /etc/nanorc
    ['#set historylog']            /etc/nanorc
    [add before '## Nanorc files'] /etc/nanorc
    [[
        # Trailing whitespaces
        syntax "all" ".*"
        icolor ,yellow "[[:space:]]+$"
    ]]
    rm ~/.nano_history
