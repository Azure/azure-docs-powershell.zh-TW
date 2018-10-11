---
title: 在 Docker 容器中執行 Azure PowerShell
description: 如何在 Docker 容器中執行 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882052"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>在 Docker 容器中執行 Azure PowerShell

Microsoft 發佈了預先安裝 Azure PowerShell 的 Docker 映像。 這些映像可讓您以 Azure PowerShell 進行實驗，或是在隔離的環境中執行。 目前已有可執行 PowerShell Core 和 PowerShell 5 的映像。 

| 環境 | Docker 映像 |
|-------------|--------------|
| Windows 上的 PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows 上的 PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux 上的 PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

若要執行上述任何容器，請使用 `docker run -it $ImageName` 取得互動終端機。 例如，若要搭配執行 Linux 容器與 PowerShell Core：

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
