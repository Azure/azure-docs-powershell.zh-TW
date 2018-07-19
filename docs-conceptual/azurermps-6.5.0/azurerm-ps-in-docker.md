---
title: 在 Docker 容器中執行 Azure PowerShell
description: 如何在 Docker 容器中執行 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110325"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>在 Docker 容器中執行 Azure PowerShell

有一組 Docker 映像會使用 Azure PowerShell 預先設定。 有兩種類型的容器可供使用：在 Windows 上執行傳統 PowerShell 的容器，以及在 Windows 或 Linux 上執行 PowerShell Core 的容器。

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

## <a name="use-a-powershell-core-container"></a>使用 PowerShell Core 容器

PowerShell Core 容器隨附 PowerShell Core v6，且會預先安裝 `AzureRM.NetCore` 模組。 執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>使用 Windows 容器搭配 PowerShell

Windows 容器已預先安裝 `AzureRM` 模組。 執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```