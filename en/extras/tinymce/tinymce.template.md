---
title: "Template"
_old_id: "1022"
_old_uri: "revo/tinymce/tinymce.template"
---

## Quick guide for adding templates TinyMCE 5

Sometimes you have a piece of code that users sometimes need to add and you want the outcome to be the same everytime.
You can with Templates in TinyMCE.

This is just a quick guide for adding templates to TinyMCE in Revolution (I found this in the forums after searching for an hour, so I thought it might be worth putting it here).

\- In the manager, goto: **System -> System settings**.

\- Choose '**TinyMCE**' in the 'core' selection box and '**General**' in the 'filter-by-area' selection box.

\- Look for the property: '**Plugins**' (key: 'tinymcerte.plugins'). Add the value '**template**' at the end of the list that is already there.

\- Change the value for the property '**Additional Settings**' (key: `tinymcerte.settings`). Add the values (templates) in a json format:

```json
{
  "templates": [
    {
      "title": "Some title 1",
      "description": "Some description 1",
      "content": "<div class='classname'><h3>Title</h3><p>Content of box.</p></div>"
    },
    {
      "title": "Some title 2",
      "description": "Some description 2",
      "url": "development.html"
    }
  ]
}
```

Note the semicolon as separators for the three necessary fields for one template. Add more by adding a comma followed by the next list.

Apparently you can use a snippet that contains the list, but I couldn't get it to work.

\- Add the value '**template**' to one of the button lists (select '**tinymcerte.toolbar1**' in the 'Filter-by-area' selection box).

Don't forget to upload the template-code in the path you just entered.

---

title: "TinyMCE"
description: "Maybe the most popular WYSIWYG editor for MODX backend"

---

## See also

1. [Spellchecker](extras/tinymce/tinymce.spellchecker)
2. [Table controls](extras/tinymce/tinymce.table-controls)
3. [TinyMCE](extras/tinymce)
