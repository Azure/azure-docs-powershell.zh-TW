---
title: Azure PowerShell 的其他安裝方式
description: 如何使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323317"
---
# <a name="other-installation-methods"></a>其他安裝方法

本文說明如何使用 MSI 或 Web Platform Installer (WebPI) 來安裝 Azure PowerShell。 您也可以從 Docker 容器內部執行 Azure PowerShell。 只有在您的系統需要時才使用這些安裝方法。 安裝 Azure PowerShell 的標準方式就是透過 PowerShellGet。 如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-azurerm-ps.md)。

若要在 Linux 或 macOS 環境上安裝，請參閱[在 macOS 或 Linux 上安裝 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>使用 Web Platform Installer 在 Windows 上安裝或更新

從 WebPI 來安裝最新版 Azure PowerShell 的方法和安裝舊版的方法一樣。
請下載 [Azure PowerShell WebPI 套件](http://aka.ms/webpi-azps)並開始安裝。

> [!NOTE]
> 如果您之前已從 PowerShell 資源庫安裝 Azure 模組，安裝程式會自動移除這些模組。 這麼做會簡化您的環境，因為它會確保您只有安裝一個 Azure PowerShell 版本。 不過，在某些情況下，您可能需要同時安裝多個版本。
>
> PowerShell 資源庫模組會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組。 相較之下，WebPI 安裝程式會在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安裝 Azure 模組。
>
> 如果安裝期間發生錯誤，請手動移除 `$env:ProgramFiles\WindowsPowerShell\Modules` 資料來中的 `Azure*` 資料夾，再重試安裝。

一旦完成安裝，您的 `$env:PSModulePath` 設定中應會有包含 Azure PowerShell Cmdlet 的目錄。 下列命令可用來確認系統是否已正確安裝 Azure PowerShell：

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> 從 WebPI 安裝時，系統可能會發生一個已知問題。 如果您的電腦因為系統更新或其他安裝而需要重新啟動，此問題可能會導致 `$env:PSModulePath` 的更新未能包含 Azure PowerShell 的安裝路徑。

嘗試在安裝之後載入或執行 Cmdlet 時，您會收到下列錯誤訊息︰

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

若要修正此錯誤，請重新啟動電腦或使用完整路徑來匯入模組。

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 套件在 Windows 上安裝或更新

您可以使用 MSI 檔案 (可從 [GitHub](https://aka.ms/azps-release) 取得) 來安裝 Azure PowerShell。 如果您已安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。 MSI 套件會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組，但不會建立版本專屬的資料夾。

## <a name="run-in-a-docker-container"></a>在 Docker 容器中執行

我們會維護使用 Azure PowerShell 預先設定的一組 Docker 映像。 有兩種類型的容器可用：在 Windows 上執行傳統 PowerShell 的容器，以及在 Windows 或 Linux 上執行 PowerShell Core 的容器。

| 環境 | Docker 映像 |
|-------------|--------------|
| Windows 上的 PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows 上的 PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux 上的 PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

若要執行上述任何容器，您要使用 `docker run -it $ImageName` 來取得互動終端機。 例如，若要在 Linux 容器上執行 PowerShell Core，請使用：

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> 若要在 Docker 中執行 Windows 容器，您的主機作業系統必須是 Windows，且 Docker 必須設為執行 Windows 容器。 若要深入了解在 Docker 中於 Windows 與 Linux 環境之間切換，請參閱 Docker 文件：[在 Windows 與 Linux 容器之間切換](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。