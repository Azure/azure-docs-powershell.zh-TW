---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: c4f2bbd4bc9e2989549304493481f56cbbf5280a
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399360"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>在 macOS 或 Linux 上安裝 Azure PowerShell

針對非 Windows 平台，可以在 PowerShell Core v6 中執行 Azure PowerShell。 這版的 PowerShell 是針對支援 .NET Core 的任何平台使用所建置。 若要使用這些平台，可以使用 .NET Standard 版本的 Azure PowerShell。

> [!NOTE]
> 目前，適用於 .NET Standard 的 Azure PowerShell 仍是搶鮮版 (Beta)。
> 若有問題或發現錯誤，請在 GitHub 中提出。
>
> * [關於Azure PowerShell 的問題](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>安裝 PowerShell Core

macOS 和大部分 Linux 發佈的 PowerShell Core 安裝指示皆不同。
您可以在下列文章中找到詳細的指示：

* [Install PowerShell Core on macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Install PowerShell Core on Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>安裝 Azure PowerShell for .NET Standard

> [!IMPORTANT]
> 其他文章中詳述的 `AzureRM` 模組無法搭配 PowerShell Core 使用。
> 您必須安裝 `Az` 模組，才能讓 Azure PowerShell 在 PowerShell Core 中發揮功能。

PowerShell Core 隨附於已安裝的 PowerShellGet 模組。 以命令啟動 PowerShell：

```bash
pwsh
```

若要安裝 Azure PowerShell，請執行下列命令：

```powershell
Install-Module Az
```

> [!NOTE]
> 如果您在嘗試安裝模組時遇到權限錯誤，可能需要以超級使用者模式執行 PowerShell，才能安裝模組。
>
> ```bash
> sudo pwsh
> ```

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答 `Yes` 或 `Yes to All` 以繼續安裝。

## <a name="enable-aliases"></a>啟用別名

為了與現有 `AzureRM` 模組相容，新的 `Az` 模組可建立具備回溯相容性的別名來使用 `AzureRM` Cmdlet。 第一次使用模組之前，請使用下列命令設定這些別名：

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

這只會設定為目前使用者的別名。 請針對其他可供 `-Scope` 使用以設定別名的值，查看 Cmdlet 的協助。

> [!NOTE]
> 如果您遇到與路徑位置有關的錯誤，請確定該路徑位置存在於您的本機系統中。 針對 `CurrentUser` 範圍，可以藉由在 `bash` 中執行下列命令來解決此錯誤：
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `Az` 載入您的 PowerShell 工作階段，然後使用您的 Azure 認證登入。 匯入模組「不」需要較高的權限。

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 自動匯入 `Az` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。
在 macOS 和 Linux 上，您應該透過 `$Profile` 環境變數來使用設定檔。 若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="next-steps"></a>後續步驟

如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。
