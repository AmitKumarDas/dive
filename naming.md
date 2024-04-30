### Learn from these snippets

```go
// First comes entity, then comes action on the entity
funcUnderTest: WithImageForPublish(
  ImagePublishSpecs{
    BuildFile:        "path/to/image.tar",
    PublishImageName: "test/my-image",
    PublishImageTag:  "latest",
  },
),
```
