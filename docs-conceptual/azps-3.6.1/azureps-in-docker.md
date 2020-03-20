---
title: 使用 Docker 中的 Azure PowerShell
description: 如何使用預先安裝在 Docker 映像中的 Azure PowerShell。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402675"
---
# <a name="using-azure-powershell-in-docker"></a>使用 Docker 中的 Azure PowerShell

我們發佈了已預先安裝 Azure PowerShell 的 Docker 映像。 此文章會示範如何開始使用 Docker 容器中的 Azure PowerShell。

## <a name="finding-available-images"></a>尋找可用的映像

發行的映像需要 Docker 17.05 或更新版本。 您也應該要能在沒有 `sudo` 或本機系統管理員權限的情況下執行 Docker。 請遵循 Docker 的官方[指示][install]以正確安裝 `docker`。

已發行的容器是從官方 PowerShell 容器建置，然後新增一層 Az 模組。

最新穩定映像包括：

- Ubuntu 18.04
- PowerShell 6.2.4 版
- Azure PowerShell 最新 Az 模組

您可以在我們的 [Docker 映像][az image]頁面上找到可用映像的完整清單。

## <a name="using-azure-powershell-in-a-container"></a>在容器中使用 Azure PowerShell

下列步驟會示範下載映像並啟動互動式 PowerShell 工作階段所需的 Docker 命令。

1. 下載最新的 azure-powershell 映像。

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. 在互動模式中執行 azure-powershell 容器：

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>使用主機驗證以互動方式執行 azure-powershell 容器

如果您已在系統裝載的 Docker 上安裝 Azure PowerShell，可能已快取 Azure 認證。 這些認證可用於在 Docker 容器中執行的 PowerShell 工作階段。

依預設，快取到的認證位於您主機上的 `$HOME/.Azure` 目錄中。 Docker 服務必須具有此位置的存取權，才能存取認證。 下列命令會啟動已裝載認證快取的容器，並啟動互動式 PowerShell 工作階段。

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>在不再需要映像時加以移除

下列命令是用來在不再需要 Docker 容器時加以刪除。

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>後續步驟

若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell