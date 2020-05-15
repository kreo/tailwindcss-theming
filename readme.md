# Tailwind CSS Theming [![GitHub release](https://img.shields.io/github/v/release/hawezo/tailwindcss-theming?include_prereleases&style=flat-square)](https://github.com/hawezo/tailwindcss-theming/releases) [![NPM release](https://img.shields.io/npm/v/tailwindcss-theming?style=flat-square)](https://npmjs.com/package/tailwindcss-theming) [![Top Language](https://img.shields.io/github/languages/top/hawezo/tailwindcss-theming?style=flat-square)]() 

[<img src="logo.svg" align="right" width="100">]()

## Table of contents

- [Introduction](#introduction)
- [Quick start](docs/quick-start.md)
- [Plugin configuration](docs/configuration.md)
    - [Changing the theme file](docs/configuration.md#changing-the-theme-file)
    - [Changing the strategy](docs/configuration.md#changing-the-strategy)
    - [Using a preset](docs/configuration.md#using-a-preset)
    - [Using variants](docs/configuration.md#using-variants)
- [Configuring your themes](docs/themes.md#configuring-your-themes)
    - [Creating a theme](docs/themes.md#creating-a-theme)
        - [Colors](docs/themes.md#colors)
        - [Variants](docs/themes.md#variants)
        - [Extending Tailwind's configuration with CSS variables](docs/themes.md#extending-tailwinds-configuration-with-css-variables)
        - [Name and targetability](docs/themes.md#name-and-targetability)
    - [Exporting your themes](docs/themes.md#exporting-your-themes)
        - [Default theme](docs/themes.md#default-theme)
        - [Default dark theme](docs/themes.md#default-dark-theme)
        - [Default light theme](docs/themes.md#default-light-theme)
        - [Additional themes](docs/themes.md#additional-themes)
- Presets (writing...)
- Example (writing...)
- [Compatibility](#compatibility)
- [Alternatives](#alternatives)

## Introduction

> **Note** - This plugin works with **Tailwind CSS v1.2** upwards.

`tailwindcss-theming` is a Tailwind CSS plugin made to solve the common need to have multiple themes in an application. It is also perfect for making dark themes.

It uses [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*) in order to make your themes interchangeable on the client-side. Swapping themes is as simple as changing a class of your `body` element. 

Moreoever, this plugin has full support for the [`prefers-color-scheme`](https://developer.mozilla.org/fr/docs/Web/CSS/@media/prefers-color-scheme) media query, so you can define a theme that will automatically be picked based on browser preferences. 

**Get started:**

```bash
$ yarn add tailwindcss-theming --dev
```

## Compatibility 

This plugin is based on [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*), which are [not compatible with IE11](https://caniuse.com/#feat=css-variables). You can have partial support for the browsers that do not support them by using a PostCSS plugin that add a fallback for CSS variables, such as [`postcss-css-variables`](https://github.com/MadLittleMods/postcss-css-variables) or [`postcss-custom-properties`](https://github.com/postcss/postcss-custom-properties). 

Keep in mind that only your default theme will work with that method.

## Alternatives 

This plugin is feature-complete, but some alternatives exist. If you're looking for a simpler approach, a different kind of configuration, or just want to know the alternatives, here is a list that you may find useful:

- [`tailwindcss-dark-mode`](https://github.com/ChanceArthur/tailwindcss-dark-mode) - If you only want the variants functionality.
- [`tailwindcss-darkmode`](https://github.com/danestves/tailwindcss-darkmode) - If you only want the variants functionality.
- [`tailwindcss-theme-swapper`](https://github.com/crswll/tailwindcss-theme-swapper) - Similar to `tailwindcss-theming`, but lower-level, and without the variant functionality.
- [Manually](https://tailwindcss.com/docs/breakpoints/#dark-mode), by adding a `screens` media query in Tailwind's configuration.
