---
title: 在 macOS 與 Linux 上安裝和設定 Azure PowerShell | Microsoft Docs
description: 如何在 macOS 與 Linux 上安裝 Azure PowerShell，以及針對初次使用來進行設定。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 3dae464a876aaebc4327ac5c834a3b3ac0eb95f6
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820420"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>在 macOS 與 Linux 上安裝和設定 Azure PowerShell

現在可以將 PowerShell Core v6 與 Azure PowerShell 安裝在非 Windows 平台上。
將 Azure PowerShell 安裝在 macOS 與 Linux 的程序與安裝在 Windows 上沒有不同，但您必須先安裝 PowerShell Core v6。

> [!NOTE]

> PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。
> 這些產品只提供有限支援。 若有問題或發現錯誤，請在 GitHub 中提出。
>
> * [關於 PowerShell Core v6 的問題](https://github.com/PowerShell/PowerShell/issues)
> * [關於Azure PowerShell 的問題](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>步驟 1：安裝 PowerShell Core v6

PowerShell Core v6 安裝程序因目標作業系統而異。
雖然 PowerShell Core v6 可以安裝在 Windows 上，但本文只說明在 macOS 與 Linux 上安裝的步驟。 如果您想要在 Windows 中使用 Azure PowerShell，請參閱 Windows 適用的[安裝](./install-azurerm-ps.md)文章。

Linux 或 macOS 上的 **PowerShell Core v6** 安裝作業會因為 Linux 發行版本和作業系統版本不同而有所差異。
您可以在下列文章中找到詳細的指示：

- [在 macOS 上安裝 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [在 Linux 上安裝 PowerShell Core](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>步驟 2：安裝 Azure PowerShell for .NET Core

PowerShell Core v6 隨附於已安裝的 PowerShellGet 模組。 這可讓您輕鬆地安裝任何已發佈到 PowerShell 資源庫的模組。 若要安裝 Azure PowerShell，請開啟新的 PowerShell 工作階段，並執行下列命令：

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>步驟 3：載入 AzureRM.Netcore 模組

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
  - 新增/設定/移除自訂環境 (例如 Azure Stack 或 Windows Azure 套件環境)
* 使用資源管理員與服務管理介面之 Azure 服務適用的管理平面 Cmdlet。
  - 虛擬機器
  - App Service (網站)
  - SQL Database
  - 儲存體
  - 網路

## <a name="next-steps"></a>後續步驟

如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。
