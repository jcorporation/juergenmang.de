---
layout: post
title: "Sphinx reStructuredText Cheatsheet"
tag: sphinx
image: /assets/garden/sphinx-rst.webp
permalink: /garden/sphinx-rst
---

My small cheatsheet for [Sphinx](https://www.sphinx-doc.org).

## Other References

- [https://trudeau.dev/cheatsheets/rst.html](https://trudeau.dev/cheatsheets/rst.html)
- [https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html](https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html)

## Toctree

- [Sphinx Documentation](https://documentation.help/Sphinx/toctree.html)

```rst
.. toctree::
   :hidden:
   :glob:
   :titlesonly:

   dir/index.rst
   *
```

## Inline Markup

```rst
*italics* is one asterisk
**bold** is two asterisks
``code`` is in backticks
```

## Headings

```rst
Heading 1
=========

Heading 2
---------

Heading 3
~~~~~~~~~
```

## Tables

```rst
+---------+-------+
| head    | head  |
+=========+=======+
| row     | row   |
+---------+-------+
|| line1  | row   |
|| line2  | row   |
+---------+-------+

or simple:

========= ====== ====================
PARAMETER TYPE   DESCRIPTION
========= ====== ====================
filename  string Filename for update.
========= ====== ====================
```

## Images

```rst
.. image:: monet_wildenstein.png
   :width: 309px
   :align: left
   :height: 208px
   :alt: Monet Wildenstein
```

## Internal Links

```rst
:doc:`Docker <010-installation/docker>`
```

## External Links

```rst
`Scrobble example`_

.. _Scrobble example: https://github.com/jcorporation/mympd-scripts/blob/main/ListenBrainz/ListenBrainz-Scrobbler.lua

or inline

`Commandline-Options <020-configuration/index.rst>`__

```

## Code

```rst
.. code:: json

   {"type": "sticker", "sticker": "like", "value": "2", "op": "=", "sort": "", "sortdesc": false, "maxentries": 200}
```

## Admonitions

- [https://sphinx-book-theme.readthedocs.io/en/stable/reference/kitchen-sink/admonitions.html](https://sphinx-book-theme.readthedocs.io/en/stable/reference/kitchen-sink/admonitions.html)

```rst
.. danger:: Do not run myMPD as root.

.. warning:: Do not run myMPD as root.

.. tip:: Do not run myMPD as root.
```

### Notes

```rst
[1]_

.. [1]

  Supported image mime types are: image/png, image/jpeg, image/webp,
  image/avif, image/svg+xml
```
