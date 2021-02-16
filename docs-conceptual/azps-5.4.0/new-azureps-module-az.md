---
title: Azure Az PowerShell 模組簡介
description: 介紹 Az PowerShell 模組，建議用於與 Azure 互動，並取代 AzureRM PowerShell 模組。
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b52b6995fb50a6ce502d42e7df588ca72340a1e7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411257"
---
# <a name="introducing-the-azure-az-powershell-module"></a><span data-ttu-id="fbf3e-103">Azure Az PowerShell 模組簡介</span><span class="sxs-lookup"><span data-stu-id="fbf3e-103">Introducing the Azure Az PowerShell module</span></span>

## <a name="overview"></a><span data-ttu-id="fbf3e-104">概觀</span><span class="sxs-lookup"><span data-stu-id="fbf3e-104">Overview</span></span>

<span data-ttu-id="fbf3e-105">Az PowerShell 模組是一組 Cmdlet，可直接從 PowerShell 管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-105">The Az PowerShell module is a set of cmdlets for managing Azure resources directly from PowerShell.</span></span> <span data-ttu-id="fbf3e-106">PowerShell 提供強大的自動化功能，可用於管理您的 Azure 資源，以取得 CI/CD 管線內容中的範例。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-106">PowerShell provides powerful features for automation that can be leveraged for managing your Azure resources for examples in the context of a CI/CD pipeline.</span></span>

<span data-ttu-id="fbf3e-107">Az PowerShell 模組取代了 AzureRM，是用來與 Azure 互動的建議版本。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-107">The Az PowerShell module is the replacement of AzureRM and is the recommended version to use for interacting with Azure.</span></span>

<span data-ttu-id="fbf3e-108">您可以使用 Az PowerShell 模組搭配下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="fbf3e-108">You can use the Az PowerShell module with one of the following methods:</span></span>

* <span data-ttu-id="fbf3e-109">[透過 PowerShellGet 安裝 Az PowerShell 模組](install-az-ps.md) (建議選項)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-109">[Install the Az PowerShell module via PowerShellGet](install-az-ps.md) (recommended option).</span></span>
* <span data-ttu-id="fbf3e-110">[透過 MSI 安裝 Az PowerShell 模組](install-az-ps-msi.md)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-110">[Install the Az PowerShell module with MSI](install-az-ps-msi.md).</span></span>
* <span data-ttu-id="fbf3e-111">[使用 Azure Cloud Shell](/azure/cloud-shell/overview)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-111">[Use Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>
* <span data-ttu-id="fbf3e-112">[使用 Az PowerShell Docker 容器](azureps-in-docker.md)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-112">[Use the Az PowerShell Docker container](azureps-in-docker.md).</span></span>

## <a name="features"></a><span data-ttu-id="fbf3e-113">功能</span><span class="sxs-lookup"><span data-stu-id="fbf3e-113">Features</span></span>

<span data-ttu-id="fbf3e-114">Az PowerShell 模組具備下列優點：</span><span class="sxs-lookup"><span data-stu-id="fbf3e-114">The Az PowerShell module features the following benefits:</span></span>

* <span data-ttu-id="fbf3e-115">安全性和穩定性</span><span class="sxs-lookup"><span data-stu-id="fbf3e-115">Security and stability</span></span>
  * <span data-ttu-id="fbf3e-116">權杖快取加密</span><span class="sxs-lookup"><span data-stu-id="fbf3e-116">Token cache encryption</span></span>
  * <span data-ttu-id="fbf3e-117">防止中間人攻擊類型</span><span class="sxs-lookup"><span data-stu-id="fbf3e-117">Prevention of man-in-the-middle attack type</span></span>
  * <span data-ttu-id="fbf3e-118">支援使用 ADFS 2019 進行驗證</span><span class="sxs-lookup"><span data-stu-id="fbf3e-118">Support authentication with ADFS 2019</span></span>
  * <span data-ttu-id="fbf3e-119">PowerShell 7 中的使用者名稱和密碼驗證</span><span class="sxs-lookup"><span data-stu-id="fbf3e-119">Username and password authentication in PowerShell 7</span></span>
  * <span data-ttu-id="fbf3e-120">支援連續存取評估等功能 (即將於 2021 推出)</span><span class="sxs-lookup"><span data-stu-id="fbf3e-120">Support for features like continuous access evaluation (coming in 2021)</span></span>
* <span data-ttu-id="fbf3e-121">支援所有 Azure 服務</span><span class="sxs-lookup"><span data-stu-id="fbf3e-121">Support for all Azure services</span></span>
  * <span data-ttu-id="fbf3e-122">所有正式發行的 Azure 服務都有對應的支援 PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="fbf3e-122">All generally available Azure services have a corresponding supported PowerShell module</span></span>
  * <span data-ttu-id="fbf3e-123">自 AzureRM 後的多個錯誤 (bug) 修正和 API 版本升級</span><span class="sxs-lookup"><span data-stu-id="fbf3e-123">Multiple bug fixes and API version upgrades since AzureRM</span></span>
* <span data-ttu-id="fbf3e-124">新功能</span><span class="sxs-lookup"><span data-stu-id="fbf3e-124">New capabilities</span></span>
  * <span data-ttu-id="fbf3e-125">Cloud Shell 和跨平台的支援</span><span class="sxs-lookup"><span data-stu-id="fbf3e-125">Support in Cloud Shell and cross-platform</span></span>
  * <span data-ttu-id="fbf3e-126">可以取得及使用存取權杖來存取 Azure 資源</span><span class="sxs-lookup"><span data-stu-id="fbf3e-126">Can get and use access token to access Azure resources</span></span>
  * <span data-ttu-id="fbf3e-127">適用於包含 Azure 資源進階 REST 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fbf3e-127">Cmdlet available for advanced REST operations with Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="fbf3e-128">PowerShell 7 和更新版本是在所有平台上與 Az PowerShell 搭配使用的 PowerShell 建議版本。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-128">PowerShell 7 and later is the recommended version of PowerShell for use with Az PowerShell on all platforms.</span></span>

<span data-ttu-id="fbf3e-129">Az PowerShell 是以 .NET Standard 程式庫為基礎，可以在所有平台 (包括 Windows、macOS 和 Linux) 上使用 PowerShell 7 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-129">The Az PowerShell module is based on the .NET Standard library and works with PowerShell 7 and later on all platforms including Windows, macOS, and Linux.</span></span> <span data-ttu-id="fbf3e-130">同時與 Windows PowerShell 5.1 相容。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-130">It's also compatible with Windows PowerShell 5.1.</span></span>

<span data-ttu-id="fbf3e-131">我們致力於將 Azure 支援帶入所有平台，而所有 Az PowerShell 模組都可跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-131">We're committed to bringing Azure support to all platforms and all Az PowerShell modules are cross-platforms.</span></span>

## <a name="upgrade-your-environment-to-az"></a><span data-ttu-id="fbf3e-132">將您的環境升級至 Az</span><span class="sxs-lookup"><span data-stu-id="fbf3e-132">Upgrade your environment to Az</span></span>

<span data-ttu-id="fbf3e-133">為了運用 PowerShell 中的最新 Azure 功能，您應盡速遷移至 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-133">To keep up with the latest Azure features in PowerShell, you should migrate to the Az module.</span></span> <span data-ttu-id="fbf3e-134">若您尚未準備好要安裝 Az 模組來取代 AzureRM，您可以透過下列方式試用 Az：</span><span class="sxs-lookup"><span data-stu-id="fbf3e-134">If you're not ready to install the Az module as a replacement for AzureRM, you have a couple of options available to experiment with Az:</span></span>

* <span data-ttu-id="fbf3e-135">在 `PowerShell` 環境中使用 [Azure Cloud Shell](/azure/cloud-shell/overview)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-135">Use a `PowerShell` environment with [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span> <span data-ttu-id="fbf3e-136">Azure Cloud Shell 是一種以瀏覽器為基礎的殼層環境，隨附有已安裝的 Az 模組，且已啟用 `Enable-AzureRM` 相容性別名。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-136">Azure Cloud Shell is a browser-based shell environment that comes with the Az module installed and `Enable-AzureRM` compatibility aliases enabled.</span></span>
* <span data-ttu-id="fbf3e-137">保留 Windows PowerShell 5.1 中安裝的 AzureRM 模組，並在 PowerShell 7 或更新版本中安裝 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-137">Keep the AzureRM module installed in Windows PowerShell 5.1 and install the Az module in PowerShell 7 or later.</span></span> <span data-ttu-id="fbf3e-138">Windows PowerShell 5.1 和 PowerShell 7 以及更新版本分別使用不同的模組集合。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-138">Windows PowerShell 5.1 and PowerShell 7 and later use separate collections of modules.</span></span> <span data-ttu-id="fbf3e-139">請依照指示安裝[最新版 PowerShell](/powershell/scripting/install/installing-powershell)，然後從 PowerShell 7 或更新版本[安裝 Az 模組](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-139">Follow the instructions to install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) and then [install the Az module](install-az-ps.md) from PowerShell 7 or later.</span></span>

<span data-ttu-id="fbf3e-140">若要從現有的 AzureRM 安裝升級：</span><span class="sxs-lookup"><span data-stu-id="fbf3e-140">To upgrade from an existing AzureRM install:</span></span>

1. [<span data-ttu-id="fbf3e-141">將 Azure PowerShell AzureRM 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="fbf3e-141">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [<span data-ttu-id="fbf3e-142">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="fbf3e-142">Install the Azure PowerShell Az module</span></span>](install-az-ps.md)
1. <span data-ttu-id="fbf3e-143">**選擇性**：當您熟悉新的命令集時，請使用 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) 啟用相容性模式來新增 AzureRM Cmdlet 的別名。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-143">**OPTIONAL**: Enable compatibility mode to add aliases for AzureRM cmdlets with [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) while you become familiar with the new command set.</span></span> <span data-ttu-id="fbf3e-144">如需詳細資訊，請參閱下一節或[開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-144">For more information, see the next section or [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a><span data-ttu-id="fbf3e-145">將現有指令碼從 Azure RM 遷移至 Az</span><span class="sxs-lookup"><span data-stu-id="fbf3e-145">Migrate existing scripts from AzureRM to Az</span></span>

<span data-ttu-id="fbf3e-146">如果您的指令碼仍以 AzureRM 模組為基礎，我們有數個資源可協助您進行移轉：</span><span class="sxs-lookup"><span data-stu-id="fbf3e-146">If your scripts are still based on the AzureRM module, we have several resources to help you with the migration:</span></span>

* [<span data-ttu-id="fbf3e-147">開始從 AzureRM 移轉至 Az</span><span class="sxs-lookup"><span data-stu-id="fbf3e-147">Get started with migration from AzureRM to Az</span></span>](migrate-from-azurerm-to-az.md)
* [<span data-ttu-id="fbf3e-148">從 AzureRM 到 Az 1.0.0 的重大變更完整清單</span><span class="sxs-lookup"><span data-stu-id="fbf3e-148">Full list of breaking changes from AzureRM to Az 1.0.0</span></span>](migrate-az-1.0.0.md)
* <span data-ttu-id="fbf3e-149">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fbf3e-149">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span></span>

## <a name="supportability"></a><span data-ttu-id="fbf3e-150">可支援性</span><span class="sxs-lookup"><span data-stu-id="fbf3e-150">Supportability</span></span>

<span data-ttu-id="fbf3e-151">Az 是最新的 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-151">Az is the most current PowerShell module for Azure.</span></span> <span data-ttu-id="fbf3e-152">若有任何問題或功能要求，您可以直接記錄在 [GitHub 存放庫](https://github.com/Azure/azure-powershell)，如果擁有支援合約，則可透過 Microsoft 支援服務直接回報。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-152">Issues or feature requests can be logged directly on the [GitHub repository](https://github.com/Azure/azure-powershell), or via Microsoft support if you have a support contract.</span></span> <span data-ttu-id="fbf3e-153">功能要求將會在最新版本的 Az 中實作。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-153">Feature requests will be implemented in the latest version of Az.</span></span> <span data-ttu-id="fbf3e-154">重大問題將會在最新的兩個 Az 版本中實作。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-154">Critical issues will be implemented on the last two versions of Az.</span></span>

<span data-ttu-id="fbf3e-155">由於 Az PowerShell 模組現在具備 AzureRM PowerShell 模組的所有功能，因此我們將于2024年2月29日淘汰 AzureRM PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-155">Because Az PowerShell modules now have all the capabilities of AzureRM PowerShell modules and more, we'll retire AzureRM PowerShell modules on 29 February 2024.</span></span>

<span data-ttu-id="fbf3e-156">若要避免服務中斷，請將使用 AzureRM PowerShell 模組的 [腳本更新為在](https://aka.ms/azpsmigrate) 2024 年2月29日之前使用 Az powershell 模組。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-156">To avoid service interruptions, [update your scripts](https://aka.ms/azpsmigrate) that use AzureRM PowerShell modules to use Az PowerShell modules by 29 February 2024.</span></span> <span data-ttu-id="fbf3e-157">若要自動更新您的腳本，請遵循 [快速入門手冊](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-157">To automatically update your scripts, follow the [quickstart guide](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically).</span></span>

## <a name="data-collection"></a><span data-ttu-id="fbf3e-158">資料集合</span><span class="sxs-lookup"><span data-stu-id="fbf3e-158">Data collection</span></span>

<span data-ttu-id="fbf3e-159">Azure PowerShell 預設會收集遙測資料。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-159">Azure PowerShell collects telemetry data by default.</span></span> <span data-ttu-id="fbf3e-160">Microsoft 彙總收集的資料，以識別使用模式、識別常見的問題，以及改善 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-160">Microsoft aggregates collected data to identify patterns of usage to identify common issues and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="fbf3e-161">Microsoft Azure PowerShell 不會收集任何私人或個人資料。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-161">Microsoft Azure PowerShell does not collect any private or personal data.</span></span> <span data-ttu-id="fbf3e-162">例如，使用量資料有助於找出問題 (例如具有低成功率的 Cmdlet)，並協助設定工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-162">For example, the usage data helps identify issues such as cmdlets with low success and helps prioritize our work.</span></span>

<span data-ttu-id="fbf3e-163">我們非常感謝這類資料所提供的見解，但也了解不是每個人都想要傳送使用資料。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-163">While we appreciate the insights this data provides, we also understand that not everyone wants to send usage data.</span></span> <span data-ttu-id="fbf3e-164">您可以使用 [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) Cmdlet 停用資料收集。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-164">You can disable data collection with the [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet.</span></span> <span data-ttu-id="fbf3e-165">若要深入了解，您也可以閱讀我們的[隱私權聲明](https://privacy.microsoft.com/privacystatement)。</span><span class="sxs-lookup"><span data-stu-id="fbf3e-165">You can also read our [privacy statement](https://privacy.microsoft.com/privacystatement) to learn more.</span></span>
