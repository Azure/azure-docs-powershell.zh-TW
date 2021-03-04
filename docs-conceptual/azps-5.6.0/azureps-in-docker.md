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
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="72aa8-103">在 Docker 中使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="72aa8-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="72aa8-104">我們會使用預先安裝的 Azure PowerShell 來發佈 Docker 映射。</span><span class="sxs-lookup"><span data-stu-id="72aa8-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="72aa8-105">本文說明如何在 Docker 容器中開始使用 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="72aa8-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="72aa8-106">尋找可用的映射</span><span class="sxs-lookup"><span data-stu-id="72aa8-106">Finding available images</span></span>

<span data-ttu-id="72aa8-107">已發行的映射需要 Docker 17.05 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="72aa8-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="72aa8-108">此外，您也可以執行 Docker，而不需要 `sudo` 或本機系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="72aa8-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="72aa8-109">請遵循 Docker 的官方 [指示][install] 以 `docker` 正確安裝。</span><span class="sxs-lookup"><span data-stu-id="72aa8-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="72aa8-110">最新的容器映射包含最新版本的 PowerShell 和 Az 模組支援的最新 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="72aa8-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="72aa8-111">針對 Az 模組的每個新版本，我們會針對下列作業系統發行映射：</span><span class="sxs-lookup"><span data-stu-id="72aa8-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="72aa8-112">Ubuntu 18.04 (預設) </span><span class="sxs-lookup"><span data-stu-id="72aa8-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="72aa8-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="72aa8-113">Debian 9</span></span>
- <span data-ttu-id="72aa8-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="72aa8-114">CentOs 7</span></span>

<span data-ttu-id="72aa8-115">您可以在 [Docker 映射][az image] 頁面上找到完整的可用映射清單。</span><span class="sxs-lookup"><span data-stu-id="72aa8-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="72aa8-116">在容器中使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="72aa8-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="72aa8-117">下列步驟顯示下載映射和啟動互動式 PowerShell 會話所需的 Docker 命令。</span><span class="sxs-lookup"><span data-stu-id="72aa8-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="72aa8-118">下載最新的 azure powershell 映射。</span><span class="sxs-lookup"><span data-stu-id="72aa8-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="72aa8-119">以互動模式執行 azure powershell 容器：</span><span class="sxs-lookup"><span data-stu-id="72aa8-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="72aa8-120">針對 Windows Docker 主機，您必須啟用 Docker 檔案共用，才能讓 Windows 上的本機磁片磁碟機與 Linux 容器共用。</span><span class="sxs-lookup"><span data-stu-id="72aa8-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="72aa8-121">如需詳細資訊，請參閱 [開始使用適用于 Windows 的 Docker][file-sharing]。</span><span class="sxs-lookup"><span data-stu-id="72aa8-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="72aa8-122">使用主機驗證以互動方式執行 azure powershell 容器</span><span class="sxs-lookup"><span data-stu-id="72aa8-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="72aa8-123">如果您已在裝載 Docker 的系統上安裝 Azure PowerShell，您可能已快取 Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="72aa8-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="72aa8-124">這些認證可用於 Docker 容器中執行的 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="72aa8-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="72aa8-125">根據預設，快取的認證會在 `$HOME/.Azure` 您主機上的目錄中。</span><span class="sxs-lookup"><span data-stu-id="72aa8-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="72aa8-126">Docker 服務必須有此位置的存取權，才能存取認證。</span><span class="sxs-lookup"><span data-stu-id="72aa8-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="72aa8-127">下列命令會啟動已裝載認證快取的容器，並啟動互動式 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="72aa8-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="72aa8-128">不再需要時移除映射</span><span class="sxs-lookup"><span data-stu-id="72aa8-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="72aa8-129">當您不再需要 Docker 容器時，會使用下列命令來刪除它。</span><span class="sxs-lookup"><span data-stu-id="72aa8-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="72aa8-130">下一步</span><span class="sxs-lookup"><span data-stu-id="72aa8-130">Next steps</span></span>

<span data-ttu-id="72aa8-131">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="72aa8-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
