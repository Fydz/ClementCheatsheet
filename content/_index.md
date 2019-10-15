+++
title = "IT Cheatsheet"
description = ""
+++

# IT Cheatsheets

## Informations
 * This website is my personnal cheatsheet, a document used to centralize my knowledge acquired on my own and my studies.
 * 

## Main features

* [Automatic Search]({{%relref "search/_index.md" %}})
* **Unlimited menu levels**
* [Generate RevealJS presentation]({{%relref "page-slide.md"%}}) from markdown (embededed or fullscreen page)
* Automatic next/prev buttons to navigate through menu entries
* [Image resizing, shadow...]({{%relref "create-page/page-images.md" %}})
* [Attachments files]({{%relref "shortcodes/attachments.md" %}})
* [List child pages]({{%relref "shortcodes/children/_index.md" %}})
* [Excerpt]({{%relref "shortcodes/excerpt.md"%}}) ! Include segment of content from one page in another
* [Mermaid diagram]({{%relref "shortcodes/mermaid.md" %}}) (flowchart, sequence, gantt)
* [Icons]({{%relref "shortcodes/icon.md" %}}), [Buttons]({{%relref "shortcodes/button.md" %}}), [Alerts]({{%relref "shortcodes/alert.md" %}}), [Panels]({{%relref "shortcodes/panel.md" %}}), [Tip/Note/Info/Warning boxes]({{%relref "shortcodes/notice.md" %}}), [Expand]({{%relref "shortcodes/expand.md" %}})
* [customizable look and feel]({{%relref "content-organisation/customize-style/_index.md"%}}), [theme style]({{%relref "content-organisation/customize-style/themestyle.md"%}}), [theme variants]({{%relref "content-organisation/customize-style/theme-variants.md"%}})

### Layout styles

This theme comes with two distinctive layout styles: Flex and Original. The main documentation is built with **Flex**, though available also in **[Original style](/original)**

#### Style "Flex" (default)

![](docdock-style-flex.png?classes=shadow)

#### Style "Original"

![](docdock-style-original.png?classes=shadow)

## Contribute to this documentation
Feel free to update this content, just click the **Edit this page** link displayed on top right of each page, and pullrequest it
{{%alert%}}Your modification will be deployed automatically when merged !{{%/alert%}}


## Documentation website
This current documentation has been statically generated with Hugo with a simple command : `hugo -t docdock` -- source code is [available here at GitHub {{%icon fa-github%}}](https://github.com/vjeantet/hugo-theme-docDock)

{{% panel theme="success" header="Automated deployments" footer="Netlify builds, deploys, and hosts  frontends." %}}
Automatically published and hosted thanks to [Netlify](https://www.netlify.com/).

Read more about [Automated HUGO deployments with Netlify](https://www.netlify.com/blog/2015/07/30/hosting-hugo-on-netlifyinsanely-fast-deploys/)
{{% /panel %}}
