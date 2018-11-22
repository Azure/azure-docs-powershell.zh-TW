---
title: Azure PowerShell 的其他安裝方式 | Microsoft Docs
description: 如何使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 7e59a5188dee3801a1305a693b2df8af63425eb5
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/22/2018
ms.locfileid: "52257477"
---
# <a name="other-installation-methods"></a>其他安裝方法

Azure PowerShell 有多種安裝方法。 慣用方法是搭配使用 PowerShellGet 和 PowerShell 資源庫。 您可以使用 Web Platform Installer (WebPI) 將 Azure PowerShell 安裝在 Windows 上，也可以用 GitHub 中的 MSI 檔案安裝。
 
## <a name="install-on-windows-using-the-web-platform-installer"></a>使用 Web Platform Installer 安裝在 Windows 上

從 WebPI 來安裝最新版 Azure PowerShell 的方法和安裝舊版的方法一樣。
請下載 [Azure PowerShell WebPI 套件](http://aka.ms/webpi-azps)並開始安裝。

> [!NOTE]
> 如果您之前已從 PowerShell 資源庫安裝 Azure 模組，安裝程式會自動移除這些模組。 這麼做會簡化您的環境，因為它會確保您只有安裝一個 Azure PowerShell 版本。 不過，在某些情況下，您可能需要同時安裝多個版本。
>
> PowerShell 資源庫模組會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組。 相較之下，WebPI 安裝程式會在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安裝 Azure 模組。
>
> 如果安裝期間發生錯誤，請手動移除 `$env:ProgramFiles\WindowsPowerShell\Modules` 資料來中的 Azure\* 資料夾，再重試安裝。

一旦完成安裝，您的 `$env:PSModulePath` 設定中應會有包含 Azure PowerShell Cmdlet 的目錄。 下列命令可用來確認系統是否已正確安裝 Azure PowerShell。

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> 從 WebPI 安裝時，系統可能會發生一個已知問題。 如果您的電腦因為系統更新或其他安裝而需要重新啟動，此問題可能會導致 `$env:PSModulePath` 的更新未能包含 Azure PowerShell 的安裝路徑。

嘗試在安裝之後載入或執行 Cmdlet 時，您會收到下列錯誤訊息︰

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

若要修正此錯誤，請重新啟動電腦或使用完整路徑來匯入模組。 例如︰

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>使用 MSI 套件安裝在 Windows 上

您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 取得) 來安裝 Azure PowerShell。 如果您已安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。 MSI 套件會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組，但不會建立版本專屬的資料夾。

