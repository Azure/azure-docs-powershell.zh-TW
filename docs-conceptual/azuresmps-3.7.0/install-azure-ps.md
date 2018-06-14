---
title: 安裝和設定 Azure PowerShell 服務管理模組 | Microsoft Docs
description: 如何安裝並設定 Azure PowerShell 以供第一次使用。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 5f59e5e5fec4fb721ac7548c12c906c7c8d5733e
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853758"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="81170-103">安裝 Azure PowerShell 服務管理模組</span><span class="sxs-lookup"><span data-stu-id="81170-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="81170-104">從 [PowerShell 資源庫](https://www.powershellgallery.com/)安裝 Azure PowerShell 是慣用的安裝方法。</span><span class="sxs-lookup"><span data-stu-id="81170-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="81170-105">步驟 1：安裝 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="81170-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="81170-106">從 PowerShell 資源庫安裝項目需要有 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="81170-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="81170-107">確定您有適當版本的 PowerShellGet 及其他系統需求。</span><span class="sxs-lookup"><span data-stu-id="81170-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="81170-108">執行下列命令，以查看您的系統上是否已安裝 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="81170-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="81170-109">您應該會看到類似下面的輸出：</span><span class="sxs-lookup"><span data-stu-id="81170-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="81170-110">如果您未安裝 PowerShellGet，請參閱[如何取得 PowerShellGet](#how-to-get-powershellget)。</span><span class="sxs-lookup"><span data-stu-id="81170-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="81170-111">步驟 2：安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="81170-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="81170-112">從執行身分為系統管理員的 Windows PowerShell 主控台來執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="81170-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="81170-113">Azure 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="81170-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="81170-114">當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載並安裝先前未安裝的其他任何 Azure 模組。</span><span class="sxs-lookup"><span data-stu-id="81170-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="81170-115">Azure 服務管理模組會與 Azure PowerShell Resource Manager 模組共用相依性。</span><span class="sxs-lookup"><span data-stu-id="81170-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="81170-116">如果您已安裝 Azure PowerShell Resource Manager 模組，您必須在 install 命令中新增 `-AllowClobber` 參數。</span><span class="sxs-lookup"><span data-stu-id="81170-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="81170-117">這可讓這個現有的共用相依性進行更新。</span><span class="sxs-lookup"><span data-stu-id="81170-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="81170-118">如果沒有這個參數，模組的安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="81170-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="81170-119">安裝此模組之後，您可以執行下列命令來匯入模組︰</span><span class="sxs-lookup"><span data-stu-id="81170-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="81170-120">使用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81170-120">To use the cmdlets</span></span>

<span data-ttu-id="81170-121">若要開始使用 Azure 服務管理 Cmdlet，請先登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="81170-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="81170-122">若要登入您的帳戶，請執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="81170-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="81170-123">在登入 Azure 之後，Azure PowerShell 會建立給定工作階段的內容。</span><span class="sxs-lookup"><span data-stu-id="81170-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="81170-124">該內容會包含要用於該工作階段內所有 Cmdlet 的 Azure PowerShell 環境、帳戶、租用戶和訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="81170-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="81170-125">現在您已準備好使用下列模組。</span><span class="sxs-lookup"><span data-stu-id="81170-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="81170-126">Azure 服務管理的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81170-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="81170-127">Azure PowerShell 模組經常會更新。</span><span class="sxs-lookup"><span data-stu-id="81170-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="81170-128">如果您發現 Cmdlet 的線上說明包含模組中沒有的 Cmdlet 或參數，請下載並安裝最新版的模組。</span><span class="sxs-lookup"><span data-stu-id="81170-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="81170-129">若要尋找您的模組版本，請輸入︰`(Get-Module Azure).Version`。</span><span class="sxs-lookup"><span data-stu-id="81170-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="81170-130">如需相關指令碼範例來協助您在 Azure 中自動進行一些常見工作，請參閱 [Windows Azure 指令碼中心](http://www.windowsazure.com/documentation/scripts/)。</span><span class="sxs-lookup"><span data-stu-id="81170-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="81170-131">如需有關安裝、學習、使用和自訂 Windows PowerShell 的一般資訊，請參閱[使用 Windows PowerShell 來編寫指令碼](http://go.microsoft.com/fwlink/p/?linkid=320210)。</span><span class="sxs-lookup"><span data-stu-id="81170-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="81170-132">如何取得 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="81170-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="81170-133">作業系統版本</span><span class="sxs-lookup"><span data-stu-id="81170-133">OS Version</span></span>|<span data-ttu-id="81170-134">安裝指示</span><span class="sxs-lookup"><span data-stu-id="81170-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="81170-135">我有 Windows 10 或 Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="81170-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="81170-136">內建於 OS 包含的 Windows Management Framework (WMF) 5.0</span><span class="sxs-lookup"><span data-stu-id="81170-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="81170-137">我想要升級至 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="81170-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="81170-138">安裝最新版的 WMF</span><span class="sxs-lookup"><span data-stu-id="81170-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="81170-139">我是在採用 PowerShell 3 或 PowerShell 4 的 Windows 版本上執行</span><span class="sxs-lookup"><span data-stu-id="81170-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="81170-140">取得 PackageManagement 模組</span><span class="sxs-lookup"><span data-stu-id="81170-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="81170-141">檢查 Azure PowerShell 的版本</span><span class="sxs-lookup"><span data-stu-id="81170-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="81170-142">雖然我們鼓勵您儘早升級至最新版本，但支援的 Azure PowerShell 版本有好幾個。</span><span class="sxs-lookup"><span data-stu-id="81170-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="81170-143">若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="81170-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
