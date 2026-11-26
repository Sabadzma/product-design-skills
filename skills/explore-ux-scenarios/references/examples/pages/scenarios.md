# Pages scenarios

## Empty states

- This branch has no pages.
- No pages match the active filters.

## Loading and pending states

- The page titles have loaded while translation counts are still pending. The editor applies a filter that depends on those counts.

## Error and recovery states

- The connection drops during a page save, and the editor cannot tell whether the changes were saved.

## Edge cases

- Another editor claims the same URL after the availability check passes but before the page is created.
