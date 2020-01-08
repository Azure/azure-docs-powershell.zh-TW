---
title: Azure PowerShell 的其他安裝方式 | Microsoft Docs
description: 如何使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: c0ac4f6cfb803519b8dd711d3cca0d4a4f7e6f8b
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "75722453"
---
# <a name="other-installation-methods"></a><span data-ttu-id="1f487-103">其他安裝方法</span><span class="sxs-lookup"><span data-stu-id="1f487-103">Other installation methods</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="1f487-104">Azure PowerShell 有多種安裝方法。</span><span class="sxs-lookup"><span data-stu-id="1f487-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="1f487-105">慣用方法是搭配使用 PowerShellGet 和 PowerShell 資源庫。</span><span class="sxs-lookup"><span data-stu-id="1f487-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="1f487-106">您可以使用 Web Platform Installer (WebPI) 將 Azure PowerShell 安裝在 Windows 上，也可以用 GitHub 中的 MSI 檔案安裝。</span><span class="sxs-lookup"><span data-stu-id="1f487-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="1f487-107">使用 Web Platform Installer 安裝在 Windows 上</span><span class="sxs-lookup"><span data-stu-id="1f487-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="1f487-108">從 WebPI 來安裝最新版 Azure PowerShell 的方法和安裝舊版的方法一樣。</span><span class="sxs-lookup"><span data-stu-id="1f487-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="1f487-109">請下載 [Azure PowerShell WebPI 套件](https://aka.ms/webpi-azps)並開始安裝。</span><span class="sxs-lookup"><span data-stu-id="1f487-109">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="1f487-110">如果您之前已從 PowerShell 資源庫安裝 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="1f487-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="1f487-111">這麼做會簡化您的環境，因為它會確保您只有安裝一個 Azure PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="1f487-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="1f487-112">不過，在某些情況下，您可能需要同時安裝多個版本。</span><span class="sxs-lookup"><span data-stu-id="1f487-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="1f487-113">PowerShell 資源庫模組會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組。</span><span class="sxs-lookup"><span data-stu-id="1f487-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1f487-114">相較之下，WebPI 安裝程式會在 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` 中安裝 Azure 模組。</span><span class="sxs-lookup"><span data-stu-id="1f487-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="1f487-115">如果安裝期間發生錯誤，請手動移除 `$env:ProgramFiles\WindowsPowerShell\Modules` 資料來中的 Azure\* 資料夾，再重試安裝。</span><span class="sxs-lookup"><span data-stu-id="1f487-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="1f487-116">一旦完成安裝，您的 `$env:PSModulePath` 設定中應會有包含 Azure PowerShell Cmdlet 的目錄。</span><span class="sxs-lookup"><span data-stu-id="1f487-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1f487-117">下列命令可用來確認系統是否已正確安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="1f487-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="1f487-118">從 WebPI 安裝時，系統可能會發生一個已知問題。</span><span class="sxs-lookup"><span data-stu-id="1f487-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="1f487-119">如果您的電腦因為系統更新或其他安裝而需要重新啟動，此問題可能會導致 `$env:PSModulePath` 的更新未能包含 Azure PowerShell 的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="1f487-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="1f487-120">嘗試在安裝之後載入或執行 Cmdlet 時，您會收到下列錯誤訊息︰</span><span class="sxs-lookup"><span data-stu-id="1f487-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
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

<span data-ttu-id="1f487-121">若要修正此錯誤，請重新啟動電腦或使用完整路徑來匯入模組。</span><span class="sxs-lookup"><span data-stu-id="1f487-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="1f487-122">例如：</span><span class="sxs-lookup"><span data-stu-id="1f487-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="1f487-123">使用 MSI 套件安裝在 Windows 上</span><span class="sxs-lookup"><span data-stu-id="1f487-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="1f487-124">您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 取得) 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="1f487-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="1f487-125">如果您已安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="1f487-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="1f487-126">MSI 套件會在 `$env:ProgramFiles\WindowsPowerShell\Modules` 中安裝模組，但不會建立版本專屬的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f487-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

