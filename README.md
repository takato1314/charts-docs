# charts-docs

This repository contains the Kubernetes guides and tutorials available in the [Bitnami Documentation](https://docs.bitnami.com).

The specific guides for each helm chart can be found under the `charts/` folder. The `common/` folder contains guides applicable to all the charts. The guides are written in Markdown using [Middleman](https://middlemanapp.com/) [templates](https://middlemanapp.com/basics/templating-language).

## License

Copyright &copy; 2023 Bitnami

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.

You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.

## Middleman

This project is built using [thoughtbot](https://github.com/thoughtbot/middleman-template) and [default](https://github.com/middleman/middleman-templates-default) Middleman template.

- Follow the [instructions](https://github.com/middleman/middleman#installation) on Middleman for [Getting Started](https://middlemanapp.com/basics/install).

- If you want to build this project template from your main repository,change this submodule directory (i.e. contains `.git` ) and init the template:
  
  > middleman init chart-docs -T file:///$(pwd)

- Build the project (Issue: [#2463](https://github.com/middleman/middleman-templates-default/pull/13))

  > middleman build --verbose

- Start the preview server:

  > middleman server

- The preview server allows you to build your site, by modifying the contents of the source directory, and see your changes reflected in the browser at: http://localhost:4567/.

## Ruby

- Ruby Version: 3.2.0 (UPDATED: 25/1/2023)
- [List packages](https://stackoverflow.com/a/15312189/3104587)
