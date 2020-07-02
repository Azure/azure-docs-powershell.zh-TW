---
title: 使用 Docker 中的 Azure PowerShell
description: 如何使用預先安裝在 Docker 映像中的 Azure PowerShell。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/23/2020
ms.locfileid: "85267911"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="cce02-103">使用 Docker 中的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cce02-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="cce02-104">我們發佈了已預先安裝 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="cce02-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="cce02-105">此文章會示範如何開始使用 Docker 容器中的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="cce02-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="cce02-106">尋找可用的映像</span><span class="sxs-lookup"><span data-stu-id="cce02-106">Finding available images</span></span>

<span data-ttu-id="cce02-107">發行的映像需要 Docker 17.05 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cce02-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="cce02-108">您也應該要能在沒有 `sudo` 或本機系統管理員權限的情況下執行 Docker。</span><span class="sxs-lookup"><span data-stu-id="cce02-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="cce02-109">請遵循 Docker 的官方[指示][install]以正確安裝 `docker`。</span><span class="sxs-lookup"><span data-stu-id="cce02-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="cce02-110">最新的容器映像包含最新版的 PowerShell，以及 Az 模組支援的最新 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="cce02-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="cce02-111">對於 Az 模組的每個新版本，我們會發行下列作業系統的映射：</span><span class="sxs-lookup"><span data-stu-id="cce02-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="cce02-112">Ubuntu 18.04 (預設)</span><span class="sxs-lookup"><span data-stu-id="cce02-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="cce02-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="cce02-113">Debian 9</span></span>
- <span data-ttu-id="cce02-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="cce02-114">CentOs 7</span></span>

<span data-ttu-id="cce02-115">您可以在我們的 [Docker 映像][az image]頁面上找到可用映像的完整清單。</span><span class="sxs-lookup"><span data-stu-id="cce02-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="cce02-116">在容器中使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cce02-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="cce02-117">下列步驟會示範下載映像並啟動互動式 PowerShell 工作階段所需的 Docker 命令。</span><span class="sxs-lookup"><span data-stu-id="cce02-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="cce02-118">下載最新的 azure-powershell 映像。</span><span class="sxs-lookup"><span data-stu-id="cce02-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="cce02-119">在互動模式中執行 azure-powershell 容器：</span><span class="sxs-lookup"><span data-stu-id="cce02-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="cce02-120">對於 Windows Docker 主機，必須啟用 Docker 檔案共用，才能讓 Windows 上的本機磁碟機與 Linux 容器共用。</span><span class="sxs-lookup"><span data-stu-id="cce02-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="cce02-121">如需詳細資訊，請參閱[開始使用適用於 Windows 的 Docker][file-sharing]。</span><span class="sxs-lookup"><span data-stu-id="cce02-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="cce02-122">使用主機驗證以互動方式執行 azure-powershell 容器</span><span class="sxs-lookup"><span data-stu-id="cce02-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="cce02-123">如果您已在系統裝載的 Docker 上安裝 Azure PowerShell，可能已快取 Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="cce02-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="cce02-124">這些認證可用於在 Docker 容器中執行的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="cce02-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="cce02-125">依預設，快取到的認證位於您主機上的 `$HOME/.Azure` 目錄中。</span><span class="sxs-lookup"><span data-stu-id="cce02-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="cce02-126">Docker 服務必須具有此位置的存取權，才能存取認證。</span><span class="sxs-lookup"><span data-stu-id="cce02-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="cce02-127">下列命令會啟動已裝載認證快取的容器，並啟動互動式 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="cce02-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="cce02-128">在不再需要映像時加以移除</span><span class="sxs-lookup"><span data-stu-id="cce02-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="cce02-129">下列命令是用來在不再需要 Docker 容器時加以刪除。</span><span class="sxs-lookup"><span data-stu-id="cce02-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="cce02-130">後續步驟</span><span class="sxs-lookup"><span data-stu-id="cce02-130">Next steps</span></span>

<span data-ttu-id="cce02-131">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="cce02-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
