# dotnet-models-creator-cli
A dotnet CLI to automatically create strongly typed c-sharp models. This CLI tool should be used to re-generate the wrapping C# classes whenever a content type is added or changed in Contentful.

## Usage
See the [PlatformApi README](https://github.com/tmw-center/platform-api/blob/master/README.md#auto-generated-content-type-classes).

## Building
Execute `dotnet pack` to build an updated package

## Testing Locally
After building, you can test your updated tool locally by running:

```sh
$: dotnet tool uninstall -g contentful.modelscreator.cli
$: dotnet tool install --global --add-source <path to repo>/Contentful.ModelsCreator.Cli/bin/Debug --no-cache contentful.modelscreator.cli
```

## Publishing
dotnet nuget push "Contentful.ModelsCreator.Cli/bin/Release/contentful.modelscreator.cli.<version>.nupkg" --source "github"