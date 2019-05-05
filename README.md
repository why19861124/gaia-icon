# gaia-icons

## Usage

```html
<span data-icon="camera"></span>
```

## Examples

- [Example](index.html)

## Prerequisites

### macOS

1. [Install Homebrew](https://brew.sh/)
1. Install FontForge and Yarn: `$ brew install fontforge ttfautohint yarn`
1. Link FontForge to your system: `$ brew link --overwrite fontforge`
1. Install Grunt CLI: `$ yarn global add grunt-cli`

### Ubuntu

1. Update APT repositories: `$ sudo apt-get update -qq`
1. Install FontForge: `$ sudo apt-get install -qqy fontforge ttfautohint`
1. [Install Yarn](https://yarnpkg.com/en/docs/install)
1. Install Grunt CLI: `$ yarn global add grunt-cli`

## Contributions

If you wish to make changes to the icon font you'll need to follow these steps:

1. Run `$ yarn` to get pull in all the required build tools.
1. Add, remove or change respective `.svg` files inside `images/`.
1. Run `$ grunt` to generate the gaia-icons font from SVG icons.
1. Load `index.html` locally in Mozilla Firefox and check your icon looks good.
1. Submit a pull request.
1. Module owner will review, land, and stamp a new version.

## Guidelines

For best results, it is recommended to follow these guidelines:

* Make the document 30px × 30px (In Inkscape: File > Document Properties... > Custom size).
* Make the icon 24px × 24px.
* Center the icon (In Inkscape: Object > Align and Distribute... > Align relative to page).
* Make sure to have only one `<path>` with no overlap per icon.
* Optimise the icons using [svgo](https://github.com/svg/svgo), then export to plain SVG file (`$ inkscape -l icon.svg icon.svg`).

Please also make sure new icons naming is consistent with existing ones:

* Use lower case only.
* Separate words with hyphens.
* Use meaningful words rather than acronyms (e.g. `top-left-crop-corner` instead of <span style="text-decoration:line-through">`t-l-crop-corner`</span>).

## Gaia usage

Gaia hackers, please read the introduction to ['Version controlled packages in Gaia'](https://gist.github.com/wilsonpage/3d7f636a78db66f8f1d7) to find out how to use this package in your Gaia app.

## Get a report

You can get a report of unused icons on a project by doing:

`$ node bin/report.js path/to/your/project/`

Please note, that dynamically inserted icons may still be marked as unused in the report.
