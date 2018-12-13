---
title: 使用 PowerShellGet 安裝 Azure PowerShell 'Az'
description: 如何使用 PowerShellGet 在 Windows、macOS 和 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216992"
---
# <a name="install-the-azure-powershell-az-module"></a>安裝 Azure PowerShell 'Az' 模組

本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。 這些指示適用於 Windows、macOS 和 Linux 平台。 在 Az 預覽版本中，不支援任何其他安裝方法。 

## <a name="requirements"></a>需求

Azure PowerShell 可搭配 Windows 上的 PowerShell 5.x 或任何平台上的 PowerShell 6.x 運作。 若要檢查您電腦上執行的 PowerShell 版本，請執行下列命令：

```powershell-interactive
$PSVersionTable.PSVersion
```

如果您有過時的版本或需要安裝 PowerShell，請參閱[安裝各種版本的 PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6)。 適用於您平台的安裝資訊是連結自該頁面。

## <a name="install-the-azure-powershell-module"></a>安裝 Azure PowerShell 模組

> [!IMPORTANT]
>
> 您可以同時安裝 `AzureRM` 和 `Az` 模組。 若您已安裝了兩個模組，__請勿啟用別名__。
> 啟用別名會讓 `AzureRM` Cmdlet 和 `Az` 命令別名產生衝突，且可能導致未預期的行為。
> 建議您在安裝 `Az` 模組之前，先將 `AzureRM` 解除安裝。 您可以隨時將 `AzureRM` 解除安裝，或啟用別名。 如需解除安裝作的指示，請參閱[將 Azure PowerShell 模組 (AzureRM) 解除安裝](uninstall-azurerm-ps.md)。 

若要在全域範圍安裝模組，您需要較高的權限，以從 PowerShell 資源庫安裝模組。 若要安裝 Azure PowerShell，請在提升權限的工作階段中執行下列命令 (在 Windows 上「以系統管理員身分執行」，或在 macOS 或 Linux 上使用超級使用者權限執行)：

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

如果您沒有系統管理員權限，藉由新增 `-Scope` 引數，即可為目前使用者進行安裝。

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答 `Yes` 或 `Yes to All` 以繼續安裝。

`Az` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。 安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。 因為模組的結構化方式，這可能需要幾秒鐘的時間。

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模組

您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。 這個命令「不會」將舊版解除安裝。

```powershell-interactive
Update-Module -Name Az
```

如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多個版本的 Azure PowerShell

您可以安裝多個版本的 Azure PowerShell。 若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-azurerm-ps.md)。

您可使用 `-RequiredVersion` 引數搭配 `Install-Module` 和 `Import-Module`，以載入特定版本的 `Az` 模組：

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

如果您已安裝多個版本的模組，則預設會載入最新版本。

## <a name="provide-feedback"></a>提供意見反應

如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。
若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.profile/send-feedback) Cmdlet。

## <a name="next-steps"></a>後續步驟

若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。
