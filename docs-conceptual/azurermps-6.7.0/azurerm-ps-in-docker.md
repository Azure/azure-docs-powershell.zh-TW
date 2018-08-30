---
title: 在 Docker 容器中執行 Azure PowerShell
description: 如何在 Docker 容器中執行 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/28/2018
ms.locfileid: "43019119"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="d89d8-103">在 Docker 容器中執行 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89d8-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="d89d8-104">為了讓 Azure PowerShell 在可攜式環境中順利執行，Microsoft 會發佈 Docker 映像搭配預先安裝的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="d89d8-104">To make running Azure PowerShell in portable environments easy, Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="d89d8-105">這些映像會提供 Linux 來賓執行 PowerShell Core，或搭配 PowerShell Core 或 PowerShell 5 的 Windows 來賓。</span><span class="sxs-lookup"><span data-stu-id="d89d8-105">These images offer a Linux guest running PowerShell Core, or a Windows guest with either PowerShell Core or PowerShell 5.</span></span>

| <span data-ttu-id="d89d8-106">環境</span><span class="sxs-lookup"><span data-stu-id="d89d8-106">Environment</span></span> | <span data-ttu-id="d89d8-107">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="d89d8-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="d89d8-108">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89d8-108">PowerShell on Windows</span></span> | [<span data-ttu-id="d89d8-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="d89d8-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="d89d8-110">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="d89d8-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="d89d8-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="d89d8-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="d89d8-112">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="d89d8-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="d89d8-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="d89d8-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="d89d8-114">若要執行上述任何容器，您要使用 `docker run -it $ImageName` 來取得互動終端機。</span><span class="sxs-lookup"><span data-stu-id="d89d8-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="d89d8-115">例如，若要在 Linux 容器上執行 PowerShell Core，請使用：</span><span class="sxs-lookup"><span data-stu-id="d89d8-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="d89d8-116">若要在 Docker 中執行 Windows 容器，您的主機作業系統必須是 Windows，且 Docker 必須設為執行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="d89d8-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="d89d8-117">若要深入了解在 Docker 中於 Windows 與 Linux 環境之間切換，請參閱 Docker 文件：[在 Windows 與 Linux 容器之間切換](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="d89d8-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="d89d8-118">使用 PowerShell Core 容器</span><span class="sxs-lookup"><span data-stu-id="d89d8-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="d89d8-119">PowerShell Core 容器隨附 PowerShell Core v6，且會預先安裝 `AzureRM.NetCore` 模組。</span><span class="sxs-lookup"><span data-stu-id="d89d8-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="d89d8-120">執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：</span><span class="sxs-lookup"><span data-stu-id="d89d8-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="d89d8-121">使用 Windows 容器搭配 PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89d8-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="d89d8-122">Windows 容器已預先安裝 `AzureRM` 模組。</span><span class="sxs-lookup"><span data-stu-id="d89d8-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="d89d8-123">執行 [Import-Module](/powershell/module/microsoft.powershell.core/import-module) Cmdlet，然後使用您的 Azure 帳戶登入：</span><span class="sxs-lookup"><span data-stu-id="d89d8-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
