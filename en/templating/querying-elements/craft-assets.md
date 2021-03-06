`craft.assets`
==============

You can access your site’s [assets](/en/assets.md) from your templates via `craft.assets`. It returns an {entry:templating/elementcriteriamodel:link} object.

```twig
{% for image in craft.assets.kind('image') %}
    <li><img src="{{ image.getUrl('thumb') }}" alt="{{ image.title }}"></li>
{% endfor %}
```

## Parameters

`craft.assets` supports the following parameters:

### `filename`

Only fetch the asset(s) with the given filename.

### `fixedOrder`

If set to `true`, assets will be returned in the same order as the IDs entered in the [`id`](#id) param.

### `folderId`

Only fetch assets that live within a given folder(s), referenced by its ID.

### `height`

Only fetch assets of a given height(s) in pixels.

### `id`

Only fetch the asset with the given ID(s).

### `indexBy`

Indexes the results by a given property. Possible values include `'id'` and `'title'`.

### `kind`

Only fetch assets of the given file kind.

The supported values are:

  * access
  * audio
  * compressed
  * excel
  * flash
  * html
  * illustrator
  * image
  * pdf
  * photoshop
  * php
  * powerpoint
  * text
  * video
  * word

### `limit`

Limits the results to *X* assets. Set to `null` (no limit) by default.

### `site`

The site the assets should be returned in. (Defaults to the current site locale.)

Can also use `siteId`.

### `offset`

Skips the first *X* assets. For example, if you set `offset(1)`, the would-be second asset returned becomes the first.

### `orderBy`

The order the assets should be returned in. Possible values include `'title'`, `'id'`, `'volumeId'`, `'folderId'`, `'filename'`, `'kind'`, `'width'`, `'height'`, `'size'`, `'dateCreated'`, and `'dateUpdated'`, as well as any textual custom field handles. If you want the entries to be sorted in descending order, add “`desc`” after the property name (ex: `'size desc'`). The default value is `'title asc'`.

### `relatedTo`

Only fetch assets that are related to certain other elements. (See {entry:docs/relations:link} for the syntax options.)

### `search`

Only fetch assets that match a given search query. (See {entry:docs/searching:link} for the syntax and available search attributes.)

### `size`

Only fetch assets with a given size(s) in bytes.

### `title`

Only fetch assets with the given title.

### `volume`

Only fetch assets that belong to a given asset volume(s), referenced by its handle.

### `volumeId`

Only fetch assets that belong to a given asset source(s), referenced by its ID.

### `width`

Only fetch assets of a given width(s) in pixels.