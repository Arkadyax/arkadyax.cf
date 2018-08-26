# Guide for adding products to the website

## Creating a products file
Each product should be in its own markdown file, named with underscores. E.g the project `Nice Juicy Software` should be named `nide_juicy_software.md`. Please use the whole name to avoid ambiguity.

## Adding details
The details for each product should be in the [YAML front matter](https://jekyllrb.com/docs/frontmatter/) of the file, and there should be no content out side of it, since this is not used. Markdown may be used.

All details should be specified in the order below.

| Variable | Description | Use case |
|----------|-------------|------------|
| `name` | The name of the procuct | **ALWAYS** |
| `description`   | A short, one line description of the prodcuct | **ALWAYS** |
| `date` | The date of the release of the most recent versions of the product, in the format `YYYY-MM-DD`| **ALWAYS** |
| `version` | The version of the product. Ideally should be a [semantic version](https://semver.org/), but if your product already has a system stick to that | **ALWAYS** |
| `tags` | Tags describing the product, in a comma seperated list, e.g `tags: [tool, shell, python]`. See [tags list](#tags) below. | RECCOMENDED |
| `opensource` | Either `true` or `false` Specifies whether this is an opensource or paid product respectively.` | **ALWAYS** |
| `download` | A URL pointing to a download or use link. E.g a link to a working demo on repl.it | OPTIONAL |
| `sourcecode` | A URL pointing to the source code. Probably Github | **MUST** if `opensource: true` |
| `docs` | A URL pointing to the products documentation | OPTIONAL |
| `demo` | A URL pointing to a demo of the product or the URL where it can be used |
| `price` | The price in USD, followed by a space followed by `USD`. Can specify other details as well, like `4.50 USD per month`. | If a paid product AND `opensource: false` |

# Tags

To request new tags be created please contact @IbraheemR, or email oban@arkadyax.cf

| Tag | Description |
|-----|-------------|
| `game` | Games |
| `tool` | Tools |
| `language` | Programming languages |
| `elanguage` | [Esoteric Programming languages](https://en.wikipedia.org/wiki/Esoteric_programming_language). Do not use `language` at the same time |
| `bot` | Bots |
| `editor` | Text or other media editors |
| `vm` | Virtual machines and hardware simulators |
| `compiler` | Programming language compilers |
| `executor` | Compiled language/bytecode runners and executors |
| `shell` | For shells and REPLs |
| `library` | Libraries |
| `api` | Application programming interfaces |
| `lang-python` | The python programming language |
| `lang-javascript` | The JavaScript programming language |
| `lang-html` | HTML things |
| `lang-css` | Css things |
| `lang-java` | The Java programming language |
| `lang-c` | The C programming language |
| `lang-cpp` | The C++ programming language |
| `lang-cs` | The C# programming language |
| `lcns-mit` | The MIT licence |
| `lcns-gpl3` | The GNU Public License 3.0 |




# A sample template (opensource) for you to copy and edit

`nice_juicy_software.md`
```
---
name: Nice Juicy Software
description: A .software that's really nice and juicy
date: 2018-01-01
version: v1.0.3
tags: [tool, api, lang-python, lang-javascript]
opensource: true
sourcecode: https://github.com/JuiceMan/nice_juicy_software
docs: https://juicysoft.io/docs
---
```

# A sample template (paid) for you to copy and edit

`nice_juicy_software.md`
```
---
name: Super Juicy Software
description: A software that's super duper nice and juicy.
date: 2018-01-01
version: v1.0.3
tags: [tool, api, lang-python, lang-javascript]
download: https://super.juicysoft.io/downloads
opensource: false
price: 99.99 USD per month
---
```