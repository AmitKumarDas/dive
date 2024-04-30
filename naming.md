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
