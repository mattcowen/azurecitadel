---
title: "Front Matter"
description: "Examples of Front Matter for the Hugo content."
weight: 6
menu:
  side:
    parent: 'Contributing'
---

## Introduction

Hugo uses a different Front Matter structure to Jekyll.

## Reference

* <https://gohugo.io/content-management/front-matter>

## Examples

### Index page

Example for a content area's `_index.md` markdown file.

```yaml
---
title: "Packer & Ansible"
description: "Collection of labs using Packer and Ansible to automate VM image creation."
menu:
  side:
    identifier: 'Packer & Ansible'
---
```

Note the identifier.

### Standard markdown page

```yaml
---
title: "Dynamic Inventories"
author: [ "Richard Cheney" ]
description: "Create dynamic inventories in Azure based on tags, resource groups and more."
menu:
  side:
    parent: 'Packer & Ansible'
    weight: 3
---
```

Note that the parent string matches the identifier. The weight determines the order. Default order is alphabetical.

### Series of content

For adding next, previous navigation buttons to a single page

```yaml
---
series:
- Some series title which can be anything
series_weight: 1
---
```

All single pages within a series are collected, sorted by `series_weight` and next, previous navigation is added at build time.

An example can be seen on the [**Getting Started**](/about/contributing/getting-started) page. If the user is at the first or last pages they will see a disabled, next or previous navigation button.