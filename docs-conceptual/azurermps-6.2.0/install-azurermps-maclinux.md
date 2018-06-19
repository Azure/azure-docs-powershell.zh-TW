---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323164"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>在 macOS 或 Linux 上安裝 Azure PowerShell

針對非 Windows 平台，可以在 PowerShell Core v6 的基礎上執行 Azure PowerShell。 這個產品並非是在 .NET Framework for Windows 上建置的標準 Azure PowerShell，而是針對 .NET Core 建置，可以在支援 .Net Core 執行階段的任何平台上執行。

> [!NOTE]
> PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。
> 這些產品只提供有限支援。 若有問題或發現錯誤，請在 GitHub 中提出。
>
> * [關於 PowerShell Core v6 的問題](https://github.com/PowerShell/PowerShell/issues)
> * [關於Azure PowerShell 的問題](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>安裝 PowerShell Core v6

Linux 或 macOS 上的 PowerShell Core v6 安裝作業會因為 Linux 發行版本和作業系統版本不同而有所差異。
您可以在下列文章中找到詳細的指示：

- [Install PowerShell Core on macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Install PowerShell Core on Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>安裝 Azure PowerShell for .NET Core

PowerShell Core v6 隨附於已安裝的 PowerShellGet 模組。 這可讓您輕鬆地安裝任何已發佈到 PowerShell 資源庫的模組。 若要安裝 Azure PowerShell，請開啟新的 PowerShell 工作階段，並執行下列命令：

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>載入 AzureRM.Netcore 模組

安裝模組後，您需要將模組載入您的 PowerShell 工作階段。 使用 `Import-Module`Cmdlet 載入模組，如下所示︰

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

匯入完成後，您可以嘗試使用下列命令登入 Azure，來測試新安裝的模組：

```powershell
Connect-AzureRmAccount
```

上述命令應會提示您移至 `https://aka.ms/devicelogin`，並輸入您收到的驗證碼。

## <a name="available-cmdlets"></a>可用的 Cmdlet

Azure PowerShell modules for .NET Standard 模組仍在開發中。 這些模組未提供適用於 Windows 版模組的所有 Cmdlet。 AzureRM.Netcore 模組實作了下列功能：

* 帳戶管理
  - 透過 Microsoft Azure Active Directory，以 Microsoft 帳戶、組織帳戶或服務主體登入
  - 透過 Save-AzureRmContext 將認證儲存到磁碟上，及使用 Import-AzureRmContext 載入儲存的認證
* 環境
  - 取得其他現成可用的 Microsoft Azure 環境
  - 新增/設定/移除自訂環境 (例如 Azure Stack 或 Microsoft Azure 套件環境)
* 使用資源管理員與服務管理介面之 Azure 服務適用的管理平面 Cmdlet。
  - 虛擬機器
  - App Service (網站)
  - SQL Database
  - 儲存體
  - 網路

## <a name="next-steps"></a>後續步驟

如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。
