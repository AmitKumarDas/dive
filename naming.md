### Learn from these snippets

```go
// Notes:
// - format: First comes entity, then comes action on the entity
// - struct: ImagePublishSpecs defines specs to publish an image
// - struct: PublishImageSpecs is wrong; we dont want to publish image specifications
// - field: PublishImageName ~ PublishImageNameAs ~ DestinationImageName ~ RetagImageName
// - field: PublishImageTag ~ PublishImageTagAs ~ DestinationImageTag ~ RetagImageTag

funcUnderTest: WithImageForPublish(
  ImagePublishSpecs{
    BuildFile:        "path/to/image.tar",
    PublishImageName: "test/my-image",
    PublishImageTag:  "latest",
  },
),
```

```go
// First comes entity, then comes action on the entity
funcUnderTest: WithFileForPublish(
  FilePublishSpecs{
    BuildFile:        "path/to/some.txt",
    PublishFilePath:  "some/path",
    PublishFileName:  "some.txt",
  },
),
```

```go
// Notes:
// - usage: i.downloadFile is better named than i.fileDownload
// - usage: i.downloadFile reflects the file to download
// - usage: i.fileDownload refects a function instead of an attribute
// - field: downloadFile is better in terms of naming
// - function: fileDownload is better in terms of naming

fmt.Errorf(
  "entity_name/action_name/nested_entity_name: failed to download abc file, relative_path=%q: %w",
  i.downloadFile,
  downloadErr,
)
```

