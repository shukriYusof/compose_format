[![Github Actions](https://github.com/shukriYusof/compose_format/actions/workflows/actions.yml/badge.svg)](https://github.com/shukriYusof/compose_format/actions/workflows/actions.yml)

# compose_format

Formats docker-compose files by using the distilled docker compose best practices.

## Docker Compose Files are complex

Docker Compose Files could be rather complex.
If these files are complex, there are multiple ways to write the same thing.
If there are multiple ways to format these files, these multiple ways will be used.
Means that it will be not possible to diff your files, cause everybody writes them a bit different.

## Alphabetical order vs. custom order

Sorting would be easy, if everything could be sorted alphabetically.
But in compose files the first thing mentioned for a service is the `image`.
`compose_format` aims to distill these compose format best practices into a tool.

## Comments

Usually formatting tools destroy comments. But comments contain valueable TODO-markers or other hints.
`compose_format` putted effort into supporting comments.

## Support

Note that this small utility is just valid until docker-compose has itself a format functionality.
Currently docker-compose just support the "config" switch. Which joins multiple compose files and print them in a machine-readable form.

## Usage

### Via Python

Install it via:
`pip3 install compose_format`

After that use it like

`compose_format compose-format.yml`
this will print the formatted compose file to stdout.
To let it replace the compose file add `--replace`.

### Via Docker

Use it like:
`cat docker-compose.yml | docker run -i funkwerk/compose_format`

## Features
 - Support for Version 3, 2.1, 2, and 1.
 - Support for Comments
 - Orders Services, Volumes, Networks
 - Orders Definitions
 - Orders Port and Volume Lists

## Contribution

Feel free to add issues or provide Pull Requests.
Especially when the order in some points violates the best practices.
This tool should be changed based on the evolving best practices.
