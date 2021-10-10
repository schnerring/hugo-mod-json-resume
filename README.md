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
```

Add a file `content/cv.md` with the following content to use the shortcodes:

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
