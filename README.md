<a href="https://photon-platform.net/">
    <img src="https://photon-platform.net/user/images/photon-logo-banner.png" alt="photon" title="photon" align="right" height="120" />
</a>


# photon ✴ Person

## 0.1.0

---


> structure, style and logic for content about people

- [configuration](#configuration)
- [templates](#templates)
- [scaffolds](#scaffolds)
- [scss](#scss)
- [assets](#assets)
- [languages](#languages)

# configuration
blueprints.yaml

fields:
- enabled
- built_in_css
- built_in_js

Before configuring this plugin, you should copy the `user/plugins/photon-person/photon-person.yaml` to `user/config/plugins/photon-person.yaml` and only edit that copy.

Here is the default configuration and an explanation of available options:

```
enabled: true
built_in_css: true
built_in_js: true

description: Custom Text added by the **photon-person** plugin (disable plugin to remove)
```

Note that if you use the admin plugin, a file with your configuration, and named photon-person.yaml will be saved in the `user/config/plugins/` folder once the configuration is saved in the admin.


# blueprints

```sh
blueprints
└── person.yaml
```

### Person
person.yaml
extends: article
fields:
- header.data.person
  - .@type
  - .givenName
  - .familyName
  - .email
  - .telephone
  - .url
  - header.data.person.address
    - header.data.person.address.streetAddress
    - header.data.person.address.postOfficeBoxNumber
    - header.data.person.address.addressLocality
    - header.data.person.address.addressRegion
    - header.data.person.address.postalCode
    - header.data.person.address.addressCountry

# templates

```sh
templates
├── _articles
│   ├── person-excerpt.html.twig
│   └── person.html.twig
├── _json-ld
│   └── person.html.twig
└── person.html.twig
```

# scaffolds

```sh
scaffolds
└── person.md
```

# scss

```sh
scss
├── articles
│   └── _person.scss
├── templates
│   └── _person.scss
└── person.scss
```

# assets

```sh
assets
├── person.css
├── person.css.map
└── person.js
```

# languages

```sh
languages
└── en.yaml
```


## Installation

- all photon plugins are installed as git submodules. More on that later.



## Configuration


## Usage

Select template type when creating a new page

## Credits


## To Do

- [ ] Future plans, if any


copyright &copy; 2020
