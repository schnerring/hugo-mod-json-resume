# hugo-json-resume

A [Hugo module](https://gohugo.io/hugo-modules/) containing templates to
integrate multilingual [JSON Resume](https://jsonresume.org/) data into your
Hugo website.

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

## Data Strucuture

The module reads JSON Resume data from Hugo's `data/` directory:

```text
data/
├─ json_resume/
    ├─ de.json
    ├─ en.json
```

Each file must adhere to the [JSON Resume schema](https://github.com/jsonresume/resume-schema/blob/master/schema.json)
specification. At least one file with the name `<default content language code>.json`
must exist (defaults to `en`). See also [Hugo Multilingual Mode](https://gohugo.io/content-management/multilingual/).

## Attributions

To display social icons, [Simple Icons](https://simpleicons.org/) (CC0) are
used.
