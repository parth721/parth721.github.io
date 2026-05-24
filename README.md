# partha721.github.io

This repository is a GitHub Pages site built with Jekyll.

## Prerequisites

- Ruby installed on your system
- Bundler installed
- GitHub Pages compatible gems via Bundler

## Recommended Bundler version

The project lock file requires Bundler `2.7.2`.

## Setup

1. Install Ruby and development tools (Ubuntu/Debian example):

```bash
sudo apt update
sudo apt install -y ruby-full build-essential zlib1g-dev
```

2. Install Bundler `2.7.2`:

```bash
sudo gem install bundler -v 2.7.2
```

3. Install project dependencies in the repository instead of the system gem path:

```bash
bundle _2.7.2_ config set path 'vendor/bundle'
bundle _2.7.2_ install
```

If you prefer system-wide installation, use:

```bash
sudo bundle _2.7.2_ install
```

## Run locally

```bash
bundle _2.7.2_ exec jekyll serve
```

Then open `http://127.0.0.1:4000` in your browser.

## Notes

- Use `bundle _2.7.2_ install` because the project uses `BUNDLED WITH 2.7.2` in `Gemfile.lock`.
- Using Bundler `4.0.12` or default `2.5.22` may cause compatibility issues with this repository.
- If you hit permission errors during install, prefer the `vendor/bundle` install method.
