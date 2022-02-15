# azure-pipelines-html-publisher

Azure DevOps extension that provides a task for publishing report in a HTML format and embeds it into a Build and Release pages.

### Extension

In order to see report on tab one must first use `Publish HTML` task. This is supporting task which makes html tab visible.

This task takes two parameters:

- **htmlFilePath**: which is a path to the html file
- **tabName**: which is the name of the tab displayed within Azure DevOps report.

#### Example YAML setup

```YAML
steps:
  - task: PublishHtml@1
    displayName: 'Publish HTML'
    inputs:
      tabName: 'Super duper html'
      htmlFilePath: '$(ResultsPath)/index.html'
```
