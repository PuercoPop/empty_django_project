# PuercoPop's Default django project

## Rationale

** Q) Why have use a settings module instead of a settings file? **
A) Because that way when doing custom configurations I only have to override
the differences. For example if I have a custom configuration for a subdomain,
myaccount.\*.\* I could create a *myaccount.py* file inside the settings
directory with the following

    ROOT_ULRS = ( 'myaccounts.urls' )

to overide the desired settings.

** Q) What is this from local\_settings import * non-sense? **

A) To allow easy overrriding of default/testing settings with a local
configuration

** Q) Y U SO HANDOME **

A) Sorry I like to troll

## What to do after cloning

+ Update submodules
```bash
git submodule init
git submodule update
```

+ Generate new secret key
```bash
python project/misc/generate_secret_key.py > project/settings/local\_settings.py
```

+ point to new origin
+ move pre hook commits
```bash
mv {project/misc/.git/hooks,}
```

## My Workflow
WIP

## How I like to work/organize repo
WIP

## The 'Batteries'
## project/misc

### 'generate\_secretkey.py'
generates a new secret key.

### pre-commmit hook
Does a search insde the apps directory for strings matching '# TODO' and
gathers them in the file TODO in the root directory

**TODO** runs unittests

# Closing remarks
If you found this useful drop me a line at pirata (at) gmail (dot) com
