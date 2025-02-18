# dodo-SSG

![oksmith-dodo-bird](https://user-images.githubusercontent.com/53121061/133529086-a9ef9617-3b50-488f-ac74-48b274eb90fd.jpg)

This Static Site Generator (SSG) command-line tool generates html files from txt and markdown (.md) files.

A single txt file or a folder containing txt files can be used as input.
All the html files will be created inside a new `./dist` folder.

The fist line of the text will be used as the html title and will be placed inside of a `<h1>` tag.
Users can specify a CSS stylesheet using the option `-s` or `--stylesheet`

## Requirements

Requirements to install and run:

- LTS version of [NodeJS](https://nodejs.org/en/)

## Installation

To install the dependencies, use:

```console
npm install
```

To create a symlink in the global folder, use:

```console
npm link
```

This will allow you to use `dodo-SSG` from anywhere in your system.

## Usage

```
dodo-SSG --input file.txt
dodo-SSG --input file.md
dodo-SSG -i ./folder-name
dodo-SSG -i folder-name -s [CSS Stylesheet URL]
dodo-SSG -c path-to-json
```

### JSON Configuration

You can use a JSON configuration file to pass options to `dodo-SSG`.

The JSON can accept the options `input` and `stylesheet`.
These ones will override the ones passed in the command.

The `input` option in the JSON is required.

## Example Input

###### Dodo-Facts.txt

```
DODO Facts


The dodo (Raphus cucullatus) is an extinct flightless bird that was endemic to
the island of Mauritius, east of Madagascar in the Indian Ocean.

The first recorded mention of the dodo was by Dutch sailors in 1598.
```

## Example Output

###### ./dist/Dodo-Facts.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>DODO Facts</title>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
  </head>
  <body>
    <h1>DODO Facts</h1>

    <p>
      The dodo (Raphus cucullatus) is an extinct flightless bird that was endemic to the island of
      Mauritius, east of Madagascar in the Indian Ocean.
    </p>

    <p>The first recorded mention of the dodo was by Dutch sailors in 1598.</p>
  </body>
</html>
```

## Built With

- [Yargs](https://github.com/yargs/yargs) - Used for command line arguments

## Author

- **Francesco Menghi** - [Profile](https://github.com/menghif)

## License

This project is licensed under the [MIT License](LICENSE)
