# Project-wide operations

## Creating, finding and editing across a project

## Source

github.com/Wolfy87/project-wide-operations

## Me

@OliverCaldwell - http://oli.me.uk/


# Create

Creating stuff is easy. It's even easier with projections.

## Projectile

github.com/tpope/vim-projectile


# Create

## Configuring projectile

Through JSON or a Vim script dictionary. Set up the mappings for your project.

```json
{
	"plugin/*.vim": {"command": "plugin"},
	"autoload/*.vim": {"command": "autoload"},
	"doc/*.txt": {"command": "doc"},
	"README.markdown": {"command": "doc"}
}
```


# Create

## Creating things with projectile

This creates plugin/foo.vim. Add a templates to pre-populate files.

You don't have to use "E...", opening a file that matches a mapping is also templated!

```vim
:Eplugin foo
```

```json
{
	"plugin/*.vim": {"command": "plugin", "template": ["echo 'HI'"]}
}
```


# Create

## Jumping to alternate files

Open an alternate file in a vertical split.

```vim
:AV
```

```json
{
	"syntax/*.vim": {"alternate": "indent/*.vim"},
	"indent/*.vim": {"alternate": "syntax/*.vim"}
}
```


# Find

TODO


# Find

## CtrlP

TODO


# Find

## Ag

TODO


# Find

## Linters

TODO


# Find

## All things quickfix

TODO


# Edit

TODO


# Edit

## Sed will suffice

TODO


# Edit

## Iterating buffers, getting vimmer

TODO


# Edit

## Batch line edit and write

TODO


# Edit

## Edit En Masse!

TODO


# Edit

## vim-enmasse example

TODO


# :qa!

## Closing dangerously

TODO