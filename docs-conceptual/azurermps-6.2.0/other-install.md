---
title: Azure PowerShell 的其他安裝方式
description: 如何使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323317"
---
# <a name="other-installation-methods"></a><span data-ttu-id="c52db-103">其他安裝方法</span><span class="sxs-lookup"><span data-stu-id="c52db-103">Other installation methods</span></span>

<span data-ttu-id="c52db-104">本文說明如何使用 MSI 或 Web Platform Installer (WebPI) 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="c52db-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="c52db-105">您也可以從 Docker 容器內部執行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="c52db-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="c52db-106">只有在您的系統需要時才使用這些安裝方法。</span><span class="sxs-lookup"><span data-stu-id="c52db-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="c52db-107">安裝 Azure PowerShell 的標準方式就是透過 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="c52db-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="c52db-108">如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="c52db-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="c52db-109">若要在 Linux 或 macOS 環境上安裝，請參閱[在 macOS 或 Linux 上安裝 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="c52db-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="c52db-110">使用 Web Platform Installer 在 Windows 上安裝或更新</span><span class="sxs-lookup"><span data-stu-id="c52db-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="c52db-111">從 WebPI 來安裝最新版 Azure PowerShell 的方法和安裝舊版的方法一樣。</span><span class="sxs-lookup"><span data-stu-id="c52db-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="c52db-112">請下載 [Azure PowerShell WebPI 套件](http://aka.ms/webpi-azps)並開始安裝。</span><span class="sxs-lookup"><span data-stu-id="c52db-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="c52db-113">如果您之前已從 PowerShell 資源庫安裝 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="c52db-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="c52db-114">這麼做會簡化您的環境，因為它會確保您只有安裝一個 Azure PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="c52db-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="c52db-115">不過，在某些情況下，您可能需要同時安裝多個版本。</span><span class="sxs-lookup"><span data-stu-id="c52db-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="c52db-116">PowerShell 資源庫模組會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組。</span><span class="sxs-lookup"><span data-stu-id="c52db-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="c52db-117">相較之下，WebPI 安裝程式會在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安裝 Azure 模組。</span><span class="sxs-lookup"><span data-stu-id="c52db-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="c52db-118">如果安裝期間發生錯誤，請手動移除 `$env:ProgramFiles\WindowsPowerShell\Modules` 資料來中的 `Azure*` 資料夾，再重試安裝。</span><span class="sxs-lookup"><span data-stu-id="c52db-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="c52db-119">一旦完成安裝，您的 `$env:PSModulePath` 設定中應會有包含 Azure PowerShell Cmdlet 的目錄。</span><span class="sxs-lookup"><span data-stu-id="c52db-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c52db-120">下列命令可用來確認系統是否已正確安裝 Azure PowerShell：</span><span class="sxs-lookup"><span data-stu-id="c52db-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="c52db-121">從 WebPI 安裝時，系統可能會發生一個已知問題。</span><span class="sxs-lookup"><span data-stu-id="c52db-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="c52db-122">如果您的電腦因為系統更新或其他安裝而需要重新啟動，此問題可能會導致 `$env:PSModulePath` 的更新未能包含 Azure PowerShell 的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="c52db-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="c52db-123">嘗試在安裝之後載入或執行 Cmdlet 時，您會收到下列錯誤訊息︰</span><span class="sxs-lookup"><span data-stu-id="c52db-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="c52db-124">若要修正此錯誤，請重新啟動電腦或使用完整路徑來匯入模組。</span><span class="sxs-lookup"><span data-stu-id="c52db-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="c52db-125">使用 MSI 套件在 Windows 上安裝或更新</span><span class="sxs-lookup"><span data-stu-id="c52db-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="c52db-126">您可以使用 MSI 檔案 (可從 [GitHub](https://aka.ms/azps-release) 取得) 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="c52db-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="c52db-127">如果您已安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="c52db-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="c52db-128">MSI 套件會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組，但不會建立版本專屬的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c52db-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="c52db-129">在 Docker 容器中執行</span><span class="sxs-lookup"><span data-stu-id="c52db-129">Run in a Docker container</span></span>

<span data-ttu-id="c52db-130">我們會維護使用 Azure PowerShell 預先設定的一組 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="c52db-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="c52db-131">有兩種類型的容器可用：在 Windows 上執行傳統 PowerShell 的容器，以及在 Windows 或 Linux 上執行 PowerShell Core 的容器。</span><span class="sxs-lookup"><span data-stu-id="c52db-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="c52db-132">環境</span><span class="sxs-lookup"><span data-stu-id="c52db-132">Environment</span></span> | <span data-ttu-id="c52db-133">Docker 映像</span><span class="sxs-lookup"><span data-stu-id="c52db-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="c52db-134">Windows 上的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="c52db-134">PowerShell on Windows</span></span> | [<span data-ttu-id="c52db-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="c52db-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="c52db-136">Windows 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c52db-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="c52db-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="c52db-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="c52db-138">Linux 上的 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c52db-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="c52db-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="c52db-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="c52db-140">若要執行上述任何容器，您要使用 `docker run -it $ImageName` 來取得互動終端機。</span><span class="sxs-lookup"><span data-stu-id="c52db-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="c52db-141">例如，若要在 Linux 容器上執行 PowerShell Core，請使用：</span><span class="sxs-lookup"><span data-stu-id="c52db-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="c52db-142">若要在 Docker 中執行 Windows 容器，您的主機作業系統必須是 Windows，且 Docker 必須設為執行 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="c52db-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="c52db-143">若要深入了解在 Docker 中於 Windows 與 Linux 環境之間切換，請參閱 Docker 文件：[在 Windows 與 Linux 容器之間切換](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)。</span><span class="sxs-lookup"><span data-stu-id="c52db-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>