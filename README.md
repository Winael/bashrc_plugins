# bashrc_plugins
_repository of plugins for `.bashrc`_

## How to use this repository

1. Fork the repository

2. Clone your fork

3. Add a specific section into your `$HOME/.bashrc` to manage those plugins

```bash
cat << EOF >> $HOME/.bashrc
# Persolalized definitions.
# You may want to put all your additions into separates files inside
# a conf directory ~/.bashrc.d/, instead of addind them here directly.
# See /usr/share/doc/bash-doc/examples in the bash-doc package.

BASH_PLUGINS_DIR=<path_to_your_fork>/plugins

if [ -d ${BASH_PLUGINS_DIR} ]; then

    for plugin in $(ls ${BASH_PLUGINS_DIR}); do
        source ${BASH_PLUGINS_DIR}/${plugin}
    done

fi
EOF
```

4. Source your $HOME/.bashrc

```bash
source $HOME/.bashrc
```

You're done !
