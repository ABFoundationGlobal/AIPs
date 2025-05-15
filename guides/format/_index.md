---
title: AIP Format and Templates
description: AIP Format and Templates
weight: 31
---

This document will cover:

- AIP Document Directory
- AIP Templates
- AIP Header Preamble
- AIP Content Format

## I. AIP Document Directory

```js (just using the syntax highlight)
// AIPs Document Directory
./
└─ AIPS/
|  └─ aip-x/           // `x` is the AIP Number
|  |  ├─ index.md      // main AIP Document in English
|  |  ├─ index.zh.md   // main AIP Document in Chinese
|  |  ├─ image1.png    // image used in AIP
|  |  ├─ image2.jpg    // image used in AIP
|  |  └─ filename.ext  // file used in AIP
|  └─ aip-template/    // this is the AIP Template Folder
```

### AIP Document File

AIP Doument file is `index.md` file in it's directory.

Every AIP should starts with the English version first. Each translation is translated from that English and placed in a new file using `index.lang.md` format.

### Auxiliary Files

If your AIP requires images, the image files should be included in the same directory of that AIP. When linking to an image in the AIP, use relative links such as `image.png`. Other files should follow the same pattern.

- When linking files from another AIP, it is enforced to copy that file from reference AIP directory to the working AIP directory.

- Files of `jpg`, `jpeg`, `png`, `svg` format are generally accepted.

- Files of `html`, `js` and other server-side or browser-side executable format are not accepted.

- If you must include an executable file like `js`, change the extension to `txt` instead.

## II. AIP Templates

```js (just using the syntax highlight)
// AIP Template Directory
./
└─ AIPS/
|  └─ aip-template/       // this is the General AIP Template Folder
|  |  └─ index.md         // this is the General AIP Template Document
|  └─ aip-template-nrc/   // this is the NRC Type AIP Template Folder
|  |  └─ index.md         // this is the NRC Type AIP Template Document
|  └─ aip-x/              // your AIP-X Folder
|  |  └─ index.md         // your AIP-X Document
```

To use the AIP Template, copy `aip-template` folder to `aip-x` folder and start your AIP with `aip-x/index.md`.

Current available templates:

- General AIP Template `/AIPS/aip-template/`

- AIP Template for Token (NRC) `/AIPS/aip-template-nrc/`

## III. AIP Header Preamble

Here is an example of AIP Header Preamble, **all fields listed in this example are required**.

```yaml
---
AIP: X
Title: "This is the AIP Title"
Authors: "[First Last](mailto:name@domain.ext)"
Discussions: https://url.to.discussions.ext
Status: Draft
Categories: Economic Model
Created: YYYY-MM-DD
---
# AIP Content Starts
```

### 1. AIP

```yaml
AIP: X
```

- **required**

- AIP number (this is determined by the AIP editor)

### 2. Title

```yaml
Title: "This is the AIP Title"
```

- **required**

- AIP title quoted with `" "`

### 3. Authors

```yaml
Authors: "[First Last](mailto:name@domain.ext)"
```

- **required**

- A list of the author’s or authors’ name(s) and/or username(s), or name(s) and email(s). Details are below.

{{< details "Authors Code Examples" >}}

```yaml
# Author with Email
Authors: "[First Last](mailto:name@domain.ext)"

# Author with URL
Authors: "[First Last](https://domain.ext)"

# Multiple Authors
Authors: "[Author 1](author1:name@domain.ext), [Author 2](https://author2.ext), [Author 3](mailto:aurhtor3@domain.ext)"
```

{{< /details >}}

### 4. Discussions

```yaml
Discussions: https://url.to.discussions.ext
```

- **required**

- While an AIP is a draft, a discussions-to header will indicate the mailing list or URL where the AIP is being discussed.

- No Discussions header is necessary if the AIP is being discussed privately with the author and haven't been submitted to AIPs repo yet.

- Discussions **cannot** point to GitHub pull requests.

### 5. Status

```yaml
Status: Draft
```

- **required**

- WIP, Draft, Public Call, Final etc.

- See [AIP Status](../aip-status.md) for all available status

### 6. Categories

```yaml
Categories: Economic Model
```

- **required**

- AIP currently has 5 categories: `Economic Model`, `Personnel`, `Technical`, `Community Governance` and `Business`

- This is defined by [AIP-0: AIP Genesis](../../AIPS/aip-0/index.md).

### 7. Created

```yaml
Created: YYYY-MM-DD
```

- **required**

- Date for first created in `YYYY-MM-DD` format

### 8. Updated

```yaml
Updated: YYYY-MM-DD
```

- Comma separated list of dates.

- e.g. `2020-12-23` or `2020-10-01, 2020-05-14, 2019-12-31`

### 9. Types

```yaml
Types: Standard
```

- AIP currently has 3 types: `Standard`, `NRC` and `Informational`

### 10. SupersededBy

```yaml
SupersededBy: 100
```

- The AIP Number of AIP that superseded this AIP.

- Only AIPs moved to `Active`, `Final` and later status can be added as an SupersededBy item.

### 11. Superseding

```yaml
Superseding: 50
```

- The AIP Number of AIP that _is_ or _is to be_ superseded by this AIP

- Only AIPs moved to `Active`, `Final` and later status can be added to this field.

- This field should be added since this AIP is meant to supersede another AIP, even when this AIP is still in `WIP` status.

### Last, Ordering

The order of AIP Header Preamble Item is not enforced, but it is recommended to use the order as the example below:

```yaml {linenos=true,linenostart=0}
---
AIP:
Title:
Authors:
Discussions:
Status:
SupersededBy:
Superseding:
Categories:
Types:
Created:
Updated:
---
# AIP Content Starts
```

## IV. AIP Content Format

AIP Content should be written in **Markdown** format. Markdown formatting is widely used in websites and documents, also there were dozens of implementations in many languages and software applications.

**CommonMark Spec** is a standard for Markdown and adopted by many applications. To see the latest **CommonMark Spec** please visit [https://spec.commonmark.org](https://spec.commonmark.org).

We'll provide more format examples in this document later.
