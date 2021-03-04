---
title: 在 Docker 中使用 Azure PowerShell
description: 如何使用預先安裝在 Docker 映射中的 Azure PowerShell。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881769"
---
# <a name="using-azure-powershell-in-docker"></a>在 Docker 中使用 Azure PowerShell

我們會使用預先安裝的 Azure PowerShell 來發佈 Docker 映射。 本文說明如何在 Docker 容器中開始使用 Azure PowerShell。

## <a name="finding-available-images"></a>尋找可用的映射

已發行的映射需要 Docker 17.05 或更新版本。 此外，您也可以執行 Docker，而不需要 `sudo` 或本機系統管理許可權。 請遵循 Docker 的官方 [指示][install] 以 `docker` 正確安裝。

最新的容器映射包含最新版本的 PowerShell 和 Az 模組支援的最新 Azure PowerShell 模組。

針對 Az 模組的每個新版本，我們會針對下列作業系統發行映射：

- Ubuntu 18.04 (預設) 
- Debian 9
- CentOs 7

您可以在 [Docker 映射][az image] 頁面上找到完整的可用映射清單。

## <a name="using-azure-powershell-in-a-container"></a>在容器中使用 Azure PowerShell

下列步驟顯示下載映射和啟動互動式 PowerShell 會話所需的 Docker 命令。

1. 下載最新的 azure powershell 映射。

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. 以互動模式執行 azure powershell 容器：

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

針對 Windows Docker 主機，您必須啟用 Docker 檔案共用，才能讓 Windows 上的本機磁片磁碟機與 Linux 容器共用。 如需詳細資訊，請參閱 [開始使用適用于 Windows 的 Docker][file-sharing]。

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>使用主機驗證以互動方式執行 azure powershell 容器

如果您已在裝載 Docker 的系統上安裝 Azure PowerShell，您可能已快取 Azure 認證。 這些認證可用於 Docker 容器中執行的 PowerShell 會話。

根據預設，快取的認證會在 `$HOME/.Azure` 您主機上的目錄中。 Docker 服務必須有此位置的存取權，才能存取認證。 下列命令會啟動已裝載認證快取的容器，並啟動互動式 PowerShell 會話。

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>不再需要時移除映射

當您不再需要 Docker 容器時，會使用下列命令來刪除它。

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>下一步

若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
