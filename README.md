# Moco Extension for Behat 3

[![Build Status](https://travis-ci.org/rezzza/moco-behat-extension.svg?branch=master)](https://travis-ci.org/rezzza/moco-behat-extension)

[Moco](https://github.com/dreamhead/moco) is a stub server we used to use in test env.

Here is a small extension to make its usage more friendly.

## Usage

```yml
default:
    extensions:
        Rezzza\MocoBehatExtension\MocoExtension:
            json_file: features/fixtures.yml
            hostname: 127.0.0.1
            port: 9997
    suites:
        default:
            contexts:
                - Rezzza\MocoBehatExtension\MocoContext
```

Then you just need to add `MocoWriter` as an argument of your context and tag your scenario with `@moco`

[See tests](features) for more details
