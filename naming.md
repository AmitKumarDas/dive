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
// - field: downloadFile is better named;  defines the file to download
// - function: fileDownload is better named; implies download action
// - struct: fileDownloadSpecs is better named; defines specs to download a file
// - naming: last part of the name majorly defines the target i.e. variable, function, or struct
// - E.g: fileDownload vs downloadFile vs fileDownloadSpecs

fmt.Errorf(
  "entity_name/action_name/nested_entity_name: failed to download abc file, relative_path=%q: %w",
  i.downloadFile,
  downloadErr,
)
```

```go
// Maintainer Notes:
// - If fileKind is ever made public, readers should be able to understand the intent
// - e.g. bwartifact.FileKindImage is readable & understood
// - e.g. bwartifact.FileImage is readable as well
// - e.g. bwartifact.Image is readable, but can lead to more than one interpretation
// - e.g. bwartifact.KindImage is readable, but can be erroneous
// - Since bwartifact.KindImage becomes tricky if there are more than one kind in bwartifact package

// supported file types
var (
  fileKindNA       = fileKind{} // Acts as the sentinel value
  fileKindImage    = fileKind{"image"}
  fileKindNonImage = fileKind{"non-image"} // represents non images s.a. binary, yaml, json, text, etc.
  fileKindBinary   = fileKind{"binary"}
  fileKindYAML     = fileKind{"yaml"}
  fileKindJSON     = fileKind{"json"}
)
```

```go
// Notes:
// - struct: action comes before entity while naming a struct
// - field: action comes before entity while naming the field

var file = PublishedFile{
  Status:          PublishStatusFail,
  FileKind:        nonImgOpts.kind,
  Source:          nonImgOpts.downloadFile,
  PublishFilePath: nonImgOpts.publishFilePath,
  PublishFileName: nonImgOpts.publishFileName,
}
```
