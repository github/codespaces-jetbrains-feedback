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

If you're having trouble connecting and the stack trace includes information about your SSH setup, there may be an issue with your keys.

If you have a key matching `/Users/<name>/.ssh/id_ed25519`, it's possible that this was a malformed key from connecting to codespaces with an older version of the `gh` client.

To fix this, try removing the key and going through the connectin process again. You should see a key called `codespaces.auto` in your SSH directory and the connection should succeed.

### MacOS 13 (Ventura)

If you are running MacOS 13 (Ventura), the JetBrains Client may be blocked by OS-level security features:

![Screenshot 2022-11-08 at 11 09 15](https://user-images.githubusercontent.com/4679612/200692344-e64d5f79-07d4-481c-bba5-a1a0e3c6a370.png)

If you see the above message while attempting to connect to a codespace via the JetBrains Gateway or any compatible JetBrains IDE, you can follow these steps to resolve the issue:

1. Open `System Preferences` and navigate to `Privacy & Security`

![Screenshot 2022-11-08 at 11 09 46](https://user-images.githubusercontent.com/4679612/200692779-12131d82-ddb7-411d-8826-ceaa39887079.png)

2. Scroll down until you see the message about the JetBrains Client being blocked

![Screenshot 2022-11-08 at 11 09 54](https://user-images.githubusercontent.com/4679612/200692894-cb6c32f4-ff0d-4e1d-8906-269a84a62c85.png)

3. Click `Open Anyway`

4. Connect to your codespace

**Note:** On the first connection after allowing the JetBrains Client, you may see the following warning:
![image (1)](https://user-images.githubusercontent.com/4679612/200693247-c46774e1-261e-447f-991c-353f9aff4a77.png)

If you see this warning, click `Open` and everything should work as expected.

:bulb: You should only need to do this once- subsequent connections should work as expected.
