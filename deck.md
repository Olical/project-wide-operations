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

Do your own thing / what works best. There's no standard.


# Find

## CtrlP

Use to select a file by name within your project. (Or use :find!)


# Find

## Ag

Find a file that contains a string, REALLY quickly.


# Find

## Linters

Find issues project-wide with JSHint, for example. Jump around them with quickfix.


# Find

## All things quickfix

CtrlP for names, quickfix for contents.


# Find

## Or use projections

Using the edit commands works with completion.


# Edit

Editing lots of files is tricky.


# Edit

## Sed will suffice

But it isn't in Vim...

```bash
sed -i 's/Plugin '.*\//Plugin 'tpope\//g' ~/.vimrc
```


# Edit

## Iterating buffers, getting vimmer

Nice, but might get sluggish. Feels sub-optimal. (In my opinion)


# Edit

## Batch line edit and write

What if you could edit multiple lines with Vim in one buffer, and write those changes to multiple files at once?

 * Within Vim.
 * Can use your macros and plugins.
 * Doesn't involve pre-loading buffers and iterating over them.


# Edit

## Edit En Masse!

En Masse is my first plugin, it pulls the source from a quickfix and allows you to edit each line. Then write them back again!

github.com/Wolfy87/vim-enmasse


# Edit

## vim-enmasse example

 * Run JSHint. (a plugin)
 * Execute `:EnMasse` to create an enmasse buffer from the quickfix list.
 * Fix all of the issues. (you'll see the JSHint error get echoed as you scroll)
 * Write in any way you want (:w), which will write each line to the right file!
 * All fixed with one buffer!


# :qa!

/\ pretty dangerous.