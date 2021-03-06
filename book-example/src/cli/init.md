# The init command
There is some minimal boilerplate that is the same for every new book. It's for this purpose that mdBook includes an `init` command.

The `init` command is used like this:

```bash
mdbook init
```

When using the `init` command for the first time, a couple of files will be set up for you:
```bash
book-test/
├── book
└── src
    ├── chapter_1.md
    └── SUMMARY.md
```

- The `src` directory is were you write your book in markdown. It contains all the source files,
configuration files, etc.

- The `book` directory is where your book is rendered. All the output is ready to be uploaded
to a server to be seen by your audience.

- The `SUMMARY.md` file is the most important file, it's the skeleton of your book and is discussed in more detail in another  [chapter](../format/summary.md)

#### Tip & Trick: Hidden Feature
When a `SUMMARY.md` file already exists, the `init` command will first parse it and generate the missing files according to the paths used in the `SUMMARY.md`. This allows you to think and create the whole structure of your book and then let mdBook generate it for you.

#### Specify a directory

When using the `init` command, you can also specify a directory, instead of using the current working directory,
by appending a path to the command:

```bash
mdbook init path/to/book
```

## --theme

When you use the `--theme` argument, the default theme will be copied into a directory
called `theme` in your source directory so that you can modify it.

The theme is selectively overwritten, this means that if you don't want to overwrite a
specific file, just delete it and the default file will be used.
