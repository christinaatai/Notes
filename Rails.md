# Rails

### How to protect null values

Use `&` as protection.
Example:
```
source_kit = pb_rails("source", props: { source: source, type: application.source&.source_group.code.downcase, hide_icon: true }) if application.source&.source_group.present?
```
There is a `&` after `source`. This protects the page from breaking if `source` is nil.
