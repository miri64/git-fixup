# git-fixup
## About
Git tool to automatically create a fixup commit by filename(s) or files currently in the index

## Installation
Just copy the `git-fixup` script into your `PATH`. E.g. on Linux

```sh
export PATH=$PATH:~/.local/bin/
cp git-fixup ~/.local/bin/
```

## Usage
You can either add files directly:

```sh
git fixup <filename(s)>
```

or via the index

```sh
git add [<filename(s)>]
git fixup
```

The latter is useful to add only parts of a file using `git add -p`.

If everything is in order your configured editor will open with a prepared
commit message subject line:

    fixup! <base commit message subject>

If the base commit is in master a `(master)` note will follow in the messages
body.

You can edit the body to add notes about your changes do to the files you added.
