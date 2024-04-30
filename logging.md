```go
fmt.Errorf(
  "entity_name/action_name/nested_entity_name: failed to download abc file, relative_path=%q: %w",
  i.downloadFile,
  downloadErr,
)
```
