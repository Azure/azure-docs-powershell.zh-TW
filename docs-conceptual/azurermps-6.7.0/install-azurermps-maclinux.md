---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106345"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>在 macOS 或 Linux 上安裝 Azure PowerShell

針對非 Windows 平台，可以在 PowerShell Core v6 中執行 Azure PowerShell。 這版的 PowerShell 是針對支援 .NET Core 的任何平台使用所建置。 若要使用這些平台，可以使用 .NET Core 特別版本的 Azure PowerShell。

> [!NOTE]
> PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。
> 這些產品只提供有限支援。 若有問題或發現錯誤，請在 GitHub 中提出。
>
> * [關於 PowerShell Core v6 的問題](https://github.com/PowerShell/PowerShell/issues)
> * [關於Azure PowerShell 的問題](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>安裝 PowerShell Core

macOS 和大部分 Linux 發佈的 PowerShell Core 安裝指示皆不同。
您可以在下列文章中找到詳細的指示：

* [Install PowerShell Core on macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Install PowerShell Core on Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>安裝 Azure PowerShell for .NET Core

PowerShell Core 隨附於已安裝的 PowerShellGet 模組。 安裝 PowerShell 中的模組需要較高的權限，因此必須以超級使用者身分來啟動您的工作階段：

```bash
sudo pwsh
```

若要安裝 Azure PowerShell，請執行下列命令：

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> 其他文章中詳述的 `AzureRM` 模組並非針對 .NET Core 所建置，且無法搭配 PowerShell Core 使用。 `AzureRM` 和 `AzureRM.NetCore` 都是使用相同的 Cmdlet 名稱，因此唯一的差異在於彙總套件模組的名稱，以及它們是針對哪個版本的 .NET 所建置。

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答 `Yes` 或 `Yes to All` 以繼續安裝。

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM.Netcore` 載入您的 PowerShell 工作階段，然後使用您的 Azure 認證登入。 匯入模組「不」需要較高的權限。

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。
在 macOS 和 Linux 上，您應該透過 `$Profile` 環境變數來使用設定檔。 若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="available-cmdlets"></a>可用的 Cmdlet

適用於 .NET Core 的 Azure PowerShell 模組仍在開發中。 這些模組未提供適用於 Windows 版模組的所有 Cmdlet。 AzureRM.Netcore 模組實作了下列功能：

* 帳戶管理
  * 透過 Microsoft Azure Active Directory，使用 Microsoft 帳戶、組織帳戶或服務主體登入
  * 透過 Save-AzureRmContext 將認證儲存到磁碟上，及使用 Import-AzureRmContext 載入儲存的認證
* 環境
  * 取得其他現成可用的 Microsoft Azure 環境
  * 新增/設定/移除自訂環境 (例如 Azure Stack 或 Windows Azure 套件環境)
* 使用資源管理員與服務管理介面之 Azure 服務適用的管理平面 Cmdlet。
  * 虛擬機器
  * App Service (網站)
  * SQL Database
  * 儲存體
  * 網路

## <a name="next-steps"></a>後續步驟

如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。
