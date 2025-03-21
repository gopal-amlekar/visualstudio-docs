---
title: Trust Settings for files and folders
description: Learn how to change trust settings for files and folders to keep Visual Studio secure.
author: TerryGLee
ms.author: tglee
manager: jmartens
ms.technology: vs-ide-general
ms.date: 08/18/2021
ms.topic: reference
f1_keywords:
 - VS.ToolsOptionsPages.Environment.PathTrustOptions
helpviewer_keywords:
 - "file security"
 - "folder security"
 - "mark of the web"
 - "trusted files"
 - "trusted folders"
---
# Configure trust settings for files and folders

::: moniker range=">=vs-2022"

In Visual Studio 2022 (Preview 2), we've revamped the Trust Settings functionality to show a warning whenever untrusted code in files, folders, projects, and solutions are about to be opened in the IDE.

:::image type="content" source="media/vs-2022/trusted-settings-warning-message.png" alt-text="Screenshot of the Trust Settings warning message":::

We'll add more information to this page as we continue to update the feature. Meanwhile, for the latest news, take a look at our recent blog post, [Improving developer security with Visual Studio 2022](https://devblogs.microsoft.com/visualstudio/improving-developer-security-with-visual-studio-2022/).

::: moniker-end

::: moniker range="<=vs-2019"

Visual Studio prompts for user approval before opening projects that have the [Mark of the Web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537628(v=vs.85)). For added security, you can also configure Visual Studio to prompt for user approval before opening any file or folder that has the mark of the web attribute, or that isn't designated as *trusted*. File and folder checks are disabled by default.

> [!WARNING]
> You should still ensure that the file, folder, or solution comes from a trusted person or a trusted location before approving it.

> [!NOTE]
> In Visual Studio 2022 (Preview), we've revamped the Trust Settings functionality to show a warning whenever untrusted code in files, folders, projects, and solutions are about to be opened in the IDE. To learn more, see the "Trusted Locations" section of the [Visual Studio 2022 Preview release notes](/visualstudio/releases/2022/release-notes-preview#trustedlocations-170P2), and the recent [Improving developer security with Visual Studio 2022](https://devblogs.microsoft.com/visualstudio/improving-developer-security-with-visual-studio-2022/) blog post.

## Configure trust settings

To change trust settings, follow these steps:

1. Open **Tools** > **Options** > **Trust Settings** and select the **Configure Trust Settings** link in the right-hand pane.

2. Choose the level of checks you'd like for files and folders. You can have different checks for each one. The options are:

   * **No verification**: Visual Studio doesn't perform any checks.

   * **Verify mark of the web attribute**: If the file or folder has the mark of the web attribute, Visual Studio blocks and asks for permission to open.

   * **Verify path is trusted**: If the file or folder path isn't part of the **Trusted Paths** list, Visual Studio blocks and asks for permission to open.

   ![Trust verification options](media/trust-settings.png)

## Add trusted paths

To add trusted paths, follow these steps:

1. Open **Tools** > **Options** > **Trust Settings** and select the **Configure Trust Settings** link in the right-hand pane.

2. Click **Add** in the **Trust Settings** dialog, and then select **File** or **Folder**.

3. Navigate to and select the file or folder you want to add to the trusted list.

   The file or folder path appears in the **Trusted Paths** list.

   ![Added trusted paths](media/trusted-paths.png)

## Remove trusted paths

To remove trusted paths, follow these steps:

1. Open **Tools** > **Options** > **Trust Settings** and select the **Configure Trust Settings** link in the right-hand pane.

2. Select the path you'd like to remove in the **Trusted Paths** list, and then click **Remove**.

   > [!TIP]
   > To select multiple entries, hold down **Shift** while you select the paths.

   The selected paths are removed from the **Trusted Paths** list.

::: moniker-end

## See also

[Build an application in Visual Studio](../walkthrough-building-an-application.md)
