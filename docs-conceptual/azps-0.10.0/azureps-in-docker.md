---
title: 使用 Docker 中的 Azure PowerShell
description: 如何使用預先安裝在 Docker 映像中的 Azure PowerShell。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445810"
---
# <a name="using-azure-powershell-in-docker"></a>使用 Docker 中的 Azure PowerShell

我們發佈了已預先安裝 Azure PowerShell 的 Docker 映像。 此文章會示範如何開始使用 Docker 容器中的 Azure PowerShell。

## <a name="finding-available-images"></a>尋找可用的映像

發行的映像需要 Docker 17.05 或更新版本。 您也應該要能在沒有 `sudo` 或本機系統管理員權限的情況下執行 Docker。 請遵循 Docker 的官方[指示][install]以正確安裝 `docker`。

最新的容器映像包含最新版的 PowerShell，以及 Az 模組支援的最新 Azure PowerShell 模組。

對於 Az 模組的每個新版本，我們會發行下列作業系統的映射：

- Ubuntu 18.04 (預設)
- Debian 9
- CentOs 7

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

對於 Windows Docker 主機，必須啟用 Docker 檔案共用，才能讓 Windows 上的本機磁碟機與 Linux 容器共用。 如需詳細資訊，請參閱[開始使用適用於 Windows 的 Docker][file-sharing]。

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
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
