# Codespaces Plugin for the JetBrains Gateway

The Codespaces team is currently partnering with JetBrains to provide a first-class experience in the JetBrains product at allow you to connect to and develop using your favorite JetBrains based IDE on an existing Codespace.

The following document provides instructions for downloading and installing the plugin and connecting to your first Codespaces. The document assumes that you have access to GitHub Codespaces and have already created a Codespace at http://github.com or using the GitHub CLI.

## How to provide feedback

We would love to hear your feedback or notice of any and all bugs you find. Please file an issue in this repository and our dev team will work to address your feedback ASAP.

## Prerequisites

This version of our plugin leverages the [GitHub CLI (gh)](https://cli.github.com/). As such `gh` needs to be [installed](https://github.com/cli/cli#installation) prior to launching the JetBrains Gateway.

We require the GitHub CLI at version `2.14.0` or higher. You can check this with the following command:

```
$ gh --version
```

## Install compatible JetBrains Gateway

We use the [JetBrains Toolbox App](https://www.jetbrains.com/toolbox-app/) since it makes managing multiple versions of a JetBrains product easy. If you don't already have the JetBrains Toolbox App installed, you can download it from [here](https://www.jetbrains.com/toolbox-app/).

Once the JetBrains Toolbox is installed, open it and select `Tools`. Scroll through the `Available` list until you find the `JetBrains Gateway`, and click "Install".

<img width="444" alt="Screen Shot 2022-08-30 at 09 01 30" src="https://user-images.githubusercontent.com/4679612/187471947-eba7207f-3271-4799-8bb3-6e3a8a9eda0c.png">


## Install the Codespaces Plugin in the JetBrains Gateway

Open the JetBrains gateway and click `Install` next to the GitHub Codespaces Provider

![Screen Shot 2022-11-04 at 1 00 46 PM](https://user-images.githubusercontent.com/1105600/200660519-3a110989-b462-4beb-9e3b-5f0dbd7dca21.png)

## Common Issues

### SSH Connection Issue