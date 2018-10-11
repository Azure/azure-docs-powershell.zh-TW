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
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="c70e4-103">在 Docker 容器中執行 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c70e4-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="c70e4-104">Microsoft 發佈了預先安裝 Azure PowerShell 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="c70e4-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="c70e4-105">這些映像可讓您以 Azure PowerShell 進行實驗，或是在隔離的環境中執行。</span><span class="sxs-lookup"><span data-stu-id="c70e4-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="c70e4-106">目前已有可執行 PowerShell Core 和 PowerShell 5 的映像。</span><span class="sxs-lookup"><span data-stu-id="c70e4-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="c70e4-107">環境</span><span class="sxs-lookup"><span data-stu-id="c70e4-107">Environment</span></span> | <span data-ttu-id="c70e4-108">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="c70e4-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="c70e4-109">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="c70e4-109">PowerShell on Windows</span></span> | [<span data-ttu-id="c70e4-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="c70e4-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="c70e4-111">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c70e4-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="c70e4-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="c70e4-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="c70e4-113">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c70e4-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="c70e4-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="c70e4-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="c70e4-115">若要執行上述任何容器，請使用 `docker run -it $ImageName` 取得互動終端機。</span><span class="sxs-lookup"><span data-stu-id="c70e4-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="c70e4-116">例如，若要搭配執行 Linux 容器與 PowerShell Core：</span><span class="sxs-lookup"><span data-stu-id="c70e4-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="c70e4-117">若要在 Docker 中執行 Windows 容器，您的主機作業系統必須是 Windows，且 Docker 必須設為執行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="c70e4-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="c70e4-118">若要深入了解在 Docker 中於 Windows 與 Linux 環境之間切換，請參閱 Docker 文件：[在 Windows 與 Linux 容器之間切換](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="c70e4-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="c70e4-119">使用 PowerShell Core 容器</span><span class="sxs-lookup"><span data-stu-id="c70e4-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="c70e4-120">PowerShell Core 容器隨附 PowerShell Core v6，且會預先安裝 `AzureRM.NetCore` 模組。</span><span class="sxs-lookup"><span data-stu-id="c70e4-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="c70e4-121">執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：</span><span class="sxs-lookup"><span data-stu-id="c70e4-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="c70e4-122">使用 Windows 容器搭配 PowerShell</span><span class="sxs-lookup"><span data-stu-id="c70e4-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="c70e4-123">Windows 容器已預先安裝 `AzureRM` 模組。</span><span class="sxs-lookup"><span data-stu-id="c70e4-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="c70e4-124">執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：</span><span class="sxs-lookup"><span data-stu-id="c70e4-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
