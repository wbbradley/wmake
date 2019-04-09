# wmake
Tool to enable contextual build files

## Usage

### Setup

To setup wmake, you'll need to place an executable file called `.wmake` in your
local directory, relevant to the project that is housed there.

```
cd $YOUR_PROJECT_DIR
echo '#!/bin/bash' > .wmake
echo 'echo "TODO: invoke your build process here"' >> .wmake
```

Ensure that the `wmake` script is in your path. I typically will just place a
soft-link from my `$HOME/bin/wmake` to this directory.

```
mkdir -p $HOME/src
cd $HOME/src
git clone git@github.com:wbbradley/wmake.git
ln -s $HOME/src/wmake/wmake $HOME/bin/wmake
```

### Usage (In Terminal)

Run `wmake` from the terminal from your project directory.

```
cd $YOUR_PROJECT_DIR
wmake
```

## Tips

The purpose of this tool is to enable local build-edit-debug cycles to go
faster. In particular, you may want to script complex build invocations that are
particular to a part of your workflow, but may not need to be put into source
control.

TODO: more explaining here...
