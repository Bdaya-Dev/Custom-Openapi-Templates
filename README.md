# Custom OpenApi Templates

These are custom mustache templates for some OpenApi Generators

## Before you start

* Install/Update cli:

  ```bash
  npm install @openapitools/openapi-generator-cli -g
  ```

## To use the custom templates

1. Add this repository as a git submodule

   ```bash
   git submodule add https://github.com/Bdaya-Dev/Custom-Openapi-Templates.git _openapi-templates
   ```

1. To update the submodule to the latest version:
   * [If the submodule folder (_openapi-templates) doesn't exist] call `git submodule init`
   * `git submodule update`

## To generate api files

1. Run the cli with the specific config file:

   ```bash
   openapi-generator-cli generate -c open-generator-config.yaml --enable-post-process-file
   ```

2. If you are using `dart-dio`, also call build runner:

   ```bash
   flutter pub run build_runner build --delete-conflicting-outputs
   ```

## To get mustache files

e.g. if the generator name is `dart-dio`

```bash
openapi-generator-cli author template -g dart-dio
```
