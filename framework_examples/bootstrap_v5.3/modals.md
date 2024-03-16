---
layout: docs
title: Modals
description: How to make modals more accessible.
group: content
toc: true
---

## Bootstrap Example

```html
<div class="modal" tabindex="-1">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">Modal title</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <p>Modal body text goes here.</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

## Improvement

```html
<div class="modal" tabindex="-1" role="dialog" aria-labelledby="modalTitle" aria-hidden="true" aria-modal="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="modalTitle">Modal title</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body" id="modalBody">
        <p>Modal body text goes here.</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

- Das role="dialog" Attribut und aria-modal="true" machen klar, dass es sich um einen modalen Dialog handelt.
- aria-labelledby="modalTitle" bezieht sich auf den Titel des Dialogs, um dessen Zweck klarzumachen.
- aria-hidden="true" wird verwendet, um den Dialog anfänglich für Screenreader unsichtbar zu machen; dieses Attribut sollte dynamisch aktualisiert werden, je nachdem, ob der Dialog sichtbar ist oder nicht.