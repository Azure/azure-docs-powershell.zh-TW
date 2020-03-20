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
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="95837-103">使用 Docker 中的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="95837-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="95837-104">我們發佈了已預先安裝 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="95837-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="95837-105">此文章會示範如何開始使用 Docker 容器中的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="95837-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="95837-106">尋找可用的映像</span><span class="sxs-lookup"><span data-stu-id="95837-106">Finding available images</span></span>

<span data-ttu-id="95837-107">發行的映像需要 Docker 17.05 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="95837-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="95837-108">您也應該要能在沒有 `sudo` 或本機系統管理員權限的情況下執行 Docker。</span><span class="sxs-lookup"><span data-stu-id="95837-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="95837-109">請遵循 Docker 的官方[指示][install]以正確安裝 `docker`。</span><span class="sxs-lookup"><span data-stu-id="95837-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="95837-110">已發行的容器是從官方 PowerShell 容器建置，然後新增一層 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="95837-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="95837-111">最新穩定映像包括：</span><span class="sxs-lookup"><span data-stu-id="95837-111">The latest stable image includes:</span></span>

- <span data-ttu-id="95837-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="95837-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="95837-113">PowerShell 6.2.4 版</span><span class="sxs-lookup"><span data-stu-id="95837-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="95837-114">Azure PowerShell 最新 Az 模組</span><span class="sxs-lookup"><span data-stu-id="95837-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="95837-115">您可以在我們的 [Docker 映像][az image]頁面上找到可用映像的完整清單。</span><span class="sxs-lookup"><span data-stu-id="95837-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="95837-116">在容器中使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="95837-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="95837-117">下列步驟會示範下載映像並啟動互動式 PowerShell 工作階段所需的 Docker 命令。</span><span class="sxs-lookup"><span data-stu-id="95837-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="95837-118">下載最新的 azure-powershell 映像。</span><span class="sxs-lookup"><span data-stu-id="95837-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="95837-119">在互動模式中執行 azure-powershell 容器：</span><span class="sxs-lookup"><span data-stu-id="95837-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="95837-120">使用主機驗證以互動方式執行 azure-powershell 容器</span><span class="sxs-lookup"><span data-stu-id="95837-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="95837-121">如果您已在系統裝載的 Docker 上安裝 Azure PowerShell，可能已快取 Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="95837-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="95837-122">這些認證可用於在 Docker 容器中執行的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="95837-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="95837-123">依預設，快取到的認證位於您主機上的 `$HOME/.Azure` 目錄中。</span><span class="sxs-lookup"><span data-stu-id="95837-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="95837-124">Docker 服務必須具有此位置的存取權，才能存取認證。</span><span class="sxs-lookup"><span data-stu-id="95837-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="95837-125">下列命令會啟動已裝載認證快取的容器，並啟動互動式 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="95837-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="95837-126">在不再需要映像時加以移除</span><span class="sxs-lookup"><span data-stu-id="95837-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="95837-127">下列命令是用來在不再需要 Docker 容器時加以刪除。</span><span class="sxs-lookup"><span data-stu-id="95837-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="95837-128">後續步驟</span><span class="sxs-lookup"><span data-stu-id="95837-128">Next steps</span></span>

<span data-ttu-id="95837-129">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="95837-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell