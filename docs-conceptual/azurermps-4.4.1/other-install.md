---
title: Azure PowerShell 的其他安裝方式 | Microsoft Docs
description: 如何使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 354061987951728fd8a5802b01f3cb8b7c60a072
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819655"
---
# <a name="other-installation-methods"></a><span data-ttu-id="49de5-103">其他安裝方法</span><span class="sxs-lookup"><span data-stu-id="49de5-103">Other installation methods</span></span>

<span data-ttu-id="49de5-104">Azure PowerShell 有多種安裝方法。</span><span class="sxs-lookup"><span data-stu-id="49de5-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="49de5-105">慣用方法是搭配使用 PowerShellGet 和 PowerShell 資源庫。</span><span class="sxs-lookup"><span data-stu-id="49de5-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="49de5-106">您可以使用 Web Platform Installer (WebPI) 將 Azure PowerShell 安裝在 Windows 上，也可以用 GitHub 中的 MSI 檔案安裝。</span><span class="sxs-lookup"><span data-stu-id="49de5-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="49de5-107">Azure PowerShell 也可以安裝在 Docker 容器中。</span><span class="sxs-lookup"><span data-stu-id="49de5-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="49de5-108">使用 Web Platform Installer 安裝在 Windows 上</span><span class="sxs-lookup"><span data-stu-id="49de5-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="49de5-109">從 WebPI 來安裝最新版 Azure PowerShell 的方法和安裝舊版的方法一樣。</span><span class="sxs-lookup"><span data-stu-id="49de5-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="49de5-110">請下載 [Azure PowerShell WebPI 套件](http://aka.ms/webpi-azps)並開始安裝。</span><span class="sxs-lookup"><span data-stu-id="49de5-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="49de5-111">如果您之前已從 PowerShell 資源庫安裝 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="49de5-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="49de5-112">這麼做會簡化您的環境，因為它會確保您只有安裝一個 Azure PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="49de5-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="49de5-113">不過，在某些情況下，您可能需要同時安裝多個版本。</span><span class="sxs-lookup"><span data-stu-id="49de5-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="49de5-114">PowerShell 資源庫模組會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組。</span><span class="sxs-lookup"><span data-stu-id="49de5-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="49de5-115">相較之下，WebPI 安裝程式會在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安裝 Azure 模組。</span><span class="sxs-lookup"><span data-stu-id="49de5-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="49de5-116">如果安裝期間發生錯誤，請手動移除 `$env:ProgramFiles\WindowsPowerShell\Modules` 資料來中的 Azure\* 資料夾，再重試安裝。</span><span class="sxs-lookup"><span data-stu-id="49de5-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="49de5-117">一旦完成安裝，您的 `$env:PSModulePath` 設定中應會有包含 Azure PowerShell Cmdlet 的目錄。</span><span class="sxs-lookup"><span data-stu-id="49de5-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="49de5-118">下列命令可用來確認系統是否已正確安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="49de5-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="49de5-119">從 WebPI 安裝時，系統可能會發生一個已知問題。</span><span class="sxs-lookup"><span data-stu-id="49de5-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="49de5-120">如果您的電腦因為系統更新或其他安裝而需要重新啟動，此問題可能會導致 `$env:PSModulePath` 的更新未能包含 Azure PowerShell 的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="49de5-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="49de5-121">嘗試在安裝之後載入或執行 Cmdlet 時，您會收到下列錯誤訊息︰</span><span class="sxs-lookup"><span data-stu-id="49de5-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="49de5-122">若要修正此錯誤，請重新啟動電腦或使用完整路徑來匯入模組。</span><span class="sxs-lookup"><span data-stu-id="49de5-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="49de5-123">例如︰</span><span class="sxs-lookup"><span data-stu-id="49de5-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="49de5-124">使用 MSI 套件安裝在 Windows 上</span><span class="sxs-lookup"><span data-stu-id="49de5-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="49de5-125">您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 取得) 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="49de5-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="49de5-126">如果您已安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="49de5-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="49de5-127">MSI 套件會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組，但不會建立版本專屬的資料夾。</span><span class="sxs-lookup"><span data-stu-id="49de5-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="49de5-128">安裝在 Docker 容器中</span><span class="sxs-lookup"><span data-stu-id="49de5-128">Install in a Docker container</span></span>

<span data-ttu-id="49de5-129">我們會維護使用 Azure PowerShell 預先設定的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="49de5-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="49de5-130">透過 `docker run` 執行容器。</span><span class="sxs-lookup"><span data-stu-id="49de5-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="49de5-131">此外，我們將一部分的 Cmdlet 作為 PowerShell Core 容器來進行維護 。</span><span class="sxs-lookup"><span data-stu-id="49de5-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="49de5-132">若為 Mac/Linux，請使用 `latest` 映像。</span><span class="sxs-lookup"><span data-stu-id="49de5-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="49de5-133">若為 Windows，則使用 `nanoserver` 映像。</span><span class="sxs-lookup"><span data-stu-id="49de5-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="49de5-134">Azure PowerShell 是透過 [PowerShell 資源庫](https://www.powershellgallery.com/)中的 `Install-Module` 安裝在映像上。</span><span class="sxs-lookup"><span data-stu-id="49de5-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>