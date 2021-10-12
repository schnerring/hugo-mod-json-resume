# hugo-json-resume

[Hugo shortcodes](https://gohugo.io/content-management/shortcodes/) to add
structured [JSON Resume](https://jsonresume.org/) data to your [Hugo](https://gohugo.io/)
site.

## Getting Started

Initialize your Hugo site as a Hugo module:

```shell
hugo mod init example.com
```

Add the following to the `config.toml` file of your site to import the module:

```toml
[module]
  [[module.imports]]
    path = "github.com/schnerring/hugo-json-resume"
  [[module.mounts]]
    source = "node_modules/simple-icons/icons"
    target = "assets/simple-icons"
```

Install the module:

```shell
hugo mod get
```

Initialize the NPM `package.json` and install the dependencies:

```shell
hugo mod npm pack
npm install
```

The module offers a basic CSS stylesheet [assets/css/json-resume.css](./assets/css/json-resume.css)
that you can use.

Finally, add a file like `content/cv.md` to use the shortcodes:

```markdown
---
title: "CV"
draft: false
---

## Experience

{{< json-resume/work >}}

## Education

{{< json-resume/education >}}

## Volunteering

{{< json-resume/volunteer >}}

## Awards

{{< json-resume/awards >}}

## Certificates

{{< json-resume/certificates >}}

## Publications

{{< json-resume/publications >}}

## Skills

{{< json-resume/skills >}}

## Languages

{{< json-resume/languages >}}

## Interests

{{< json-resume/interests >}}

## References

{{< json-resume/references >}}

## Projects

{{< json-resume/projects >}}
```

## Attributions

To display social icons, [Simple Icons](https://simpleicons.org/) (CC0) are
used.
