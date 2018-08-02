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
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/02/2018
ms.locfileid: "39367900"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="23e9b-103">在 Docker 容器中執行 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="23e9b-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="23e9b-104">有一組 Docker 映像會使用 Azure PowerShell 預先設定。</span><span class="sxs-lookup"><span data-stu-id="23e9b-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="23e9b-105">有兩種類型的容器可供使用：在 Windows 上執行傳統 PowerShell 的容器，以及在 Windows 或 Linux 上執行 PowerShell Core 的容器。</span><span class="sxs-lookup"><span data-stu-id="23e9b-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="23e9b-106">環境</span><span class="sxs-lookup"><span data-stu-id="23e9b-106">Environment</span></span> | <span data-ttu-id="23e9b-107">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="23e9b-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="23e9b-108">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="23e9b-108">PowerShell on Windows</span></span> | [<span data-ttu-id="23e9b-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="23e9b-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="23e9b-110">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="23e9b-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="23e9b-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="23e9b-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="23e9b-112">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="23e9b-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="23e9b-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="23e9b-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="23e9b-114">若要執行上述任何容器，您要使用 `docker run -it $ImageName` 來取得互動終端機。</span><span class="sxs-lookup"><span data-stu-id="23e9b-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="23e9b-115">例如，若要在 Linux 容器上執行 PowerShell Core，請使用：</span><span class="sxs-lookup"><span data-stu-id="23e9b-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="23e9b-116">若要在 Docker 中執行 Windows 容器，您的主機作業系統必須是 Windows，且 Docker 必須設為執行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="23e9b-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="23e9b-117">若要深入了解在 Docker 中於 Windows 與 Linux 環境之間切換，請參閱 Docker 文件：[在 Windows 與 Linux 容器之間切換](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="23e9b-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="23e9b-118">使用 PowerShell Core 容器</span><span class="sxs-lookup"><span data-stu-id="23e9b-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="23e9b-119">PowerShell Core 容器隨附 PowerShell Core v6，且會預先安裝 `AzureRM.NetCore` 模組。</span><span class="sxs-lookup"><span data-stu-id="23e9b-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="23e9b-120">執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：</span><span class="sxs-lookup"><span data-stu-id="23e9b-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="23e9b-121">使用 Windows 容器搭配 PowerShell</span><span class="sxs-lookup"><span data-stu-id="23e9b-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="23e9b-122">Windows 容器已預先安裝 `AzureRM` 模組。</span><span class="sxs-lookup"><span data-stu-id="23e9b-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="23e9b-123">執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：</span><span class="sxs-lookup"><span data-stu-id="23e9b-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```