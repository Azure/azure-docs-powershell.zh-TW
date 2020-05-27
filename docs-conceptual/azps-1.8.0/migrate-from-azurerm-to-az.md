---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 0b0b951d540ed91e15472853bba46e4f302921bc
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386998"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="4e788-103">將 Azure PowerShell 從 AzureRM 移轉至 Az</span><span class="sxs-lookup"><span data-stu-id="4e788-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="4e788-104">Az 模組有 AzureRM 的功能同位，但是會使用比較短且更一致的 Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="4e788-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="4e788-105">針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。</span><span class="sxs-lookup"><span data-stu-id="4e788-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="4e788-106">為了更輕鬆進行轉換，Az 提供一些工具，讓您使用 AzureRM 執行現有的指令碼。</span><span class="sxs-lookup"><span data-stu-id="4e788-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="4e788-107">不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到新的模組。</span><span class="sxs-lookup"><span data-stu-id="4e788-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

<span data-ttu-id="4e788-108">若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱[從 AzureRM 到 Az 的完整變更](migrate-az-1.0.0.md)。</span><span class="sxs-lookup"><span data-stu-id="4e788-108">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="4e788-109">確定現有指令碼可使用最新的 AzureRM 版本</span><span class="sxs-lookup"><span data-stu-id="4e788-109">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="4e788-110">在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="4e788-110">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span> <span data-ttu-id="4e788-111">進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道必須解除安裝哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="4e788-111">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="4e788-112">若要檢查您所安裝的 AzureRM 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="4e788-112">To check which version(s) of AzureRM you have installed, run the command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

<span data-ttu-id="4e788-113">AzureRM __最新的__可用版本為 __6.13.1__。</span><span class="sxs-lookup"><span data-stu-id="4e788-113">The __latest__ available release of AzureRM is __6.13.1__.</span></span> <span data-ttu-id="4e788-114">如果您未安裝此版本，您現有的指令碼可能需要進行其他修改，才能使用此處和[重大變更清單](migrate-az-1.0.0.md)中未列出的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="4e788-114">If you don't have this version installed, your existing scripts may need additional modification to work with the Az module beyond what's described here and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="4e788-115">如果您的指令碼無法使用 AzureRM 6.13.1，請根據[從 AzureRM 5.x 移轉至 6.x 的指南](/powershell/azure/azurerm/migration-guide.6.0.0)加以更新。</span><span class="sxs-lookup"><span data-stu-id="4e788-115">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span>
<span data-ttu-id="4e788-116">如果您使用舊版的 AzureRM 模組，請參考各個主要版本適用的移轉指南。</span><span class="sxs-lookup"><span data-stu-id="4e788-116">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="uninstall-azurerm"></a><span data-ttu-id="4e788-117">解除安裝 AzureRM</span><span class="sxs-lookup"><span data-stu-id="4e788-117">Uninstall AzureRM</span></span>

<span data-ttu-id="4e788-118">Az 模組不保證能與 PowerShell 5.1 for Windows 中任何現有的 AzureRM 安裝相容。</span><span class="sxs-lookup"><span data-stu-id="4e788-118">The Az module is not guaranteed to be compatible with any existing AzureRM installs in PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="4e788-119">在安裝 Az 模組之前，請先[解除安裝 AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)。</span><span class="sxs-lookup"><span data-stu-id="4e788-119">Before you install the Az module, [uninstall AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4e788-120">如果您尚未準備好要從系統中移除 AzureRM 模組，您可以改為安裝適用於 [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x 或更新版本的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="4e788-120">If you're not ready to remove the AzureRM module from your system, you can install the Az module for [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x or later instead.</span></span> <span data-ttu-id="4e788-121">PowerShell Core 與 PowerShell 5.1 for Windows 使用不同的模組程式庫，因此不會有任何衝突。</span><span class="sxs-lookup"><span data-stu-id="4e788-121">PowerShell Core and PowerShell 5.1 for Windows use different module libraries, so there will be no conflicts.</span></span> <span data-ttu-id="4e788-122">您仍然可以在 PowerShell Core 中[啟用別名](#enable-azurerm-compatibility-aliases)。</span><span class="sxs-lookup"><span data-stu-id="4e788-122">You can still [enable aliases](#enable-azurerm-compatibility-aliases) in PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="4e788-123">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="4e788-123">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="4e788-124">第一個步驟是在您的平台上安裝 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="4e788-124">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="4e788-125">當您安裝 Az 時，建議您先解除安裝 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="4e788-125">When you install Az, it's recommended that you uninstall AzureRM.</span></span> <span data-ttu-id="4e788-126">在下列步驟中，您將了解如何繼續執行現有的指令碼，並且讓舊的 Cmdlet 名稱相容。</span><span class="sxs-lookup"><span data-stu-id="4e788-126">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="4e788-127">若要安裝 Azure PowerShell Az 模組，請依照[安裝 Az 模組](install-az-ps.md)中的指示操作。</span><span class="sxs-lookup"><span data-stu-id="4e788-127">To install the Azure PowerShell Az module, follow the instructions in [Install the Az module](install-az-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4e788-128">此時，您可以執行 Az 模組中提供的 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) Cmdlet，以確保所有版本的 AzureRM 都已解除安裝，而不會造成衝突。</span><span class="sxs-lookup"><span data-stu-id="4e788-128">At this point, you might want to run the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet provided in the Az module, just to make sure that all versions of AzureRM have been uninstalled and won't cause conflicts.</span></span>

## <a name="enable-azurerm-compatibility-aliases"></a><span data-ttu-id="4e788-129">啟用 AzureRM 相容性別名</span><span class="sxs-lookup"><span data-stu-id="4e788-129">Enable AzureRM compatibility aliases</span></span>

<span data-ttu-id="4e788-130">在 AzureRM 已解除安裝且指令碼使用最新 AzureRM 版本的情況下，下一個步驟是啟用 Az 模組的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="4e788-130">With AzureRM uninstalled and your scripts working with the latest AzureRM version, the next step is to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="4e788-131">透過以下命令啟用相容性：</span><span class="sxs-lookup"><span data-stu-id="4e788-131">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="4e788-132">別名讓您能夠使用舊的 Cmdlet 名稱搭配已安裝的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="4e788-132">Aliases enable the ability to use old cmdlet names with the Az module installed.</span></span> <span data-ttu-id="4e788-133">這些別名會寫入至所選範圍的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e788-133">These aliases are written to the profile for the selected scope.</span></span> <span data-ttu-id="4e788-134">如果沒有設定檔存在，則會建立一個。</span><span class="sxs-lookup"><span data-stu-id="4e788-134">If no profile exists, one is created.</span></span>
<span data-ttu-id="4e788-135">使用大於 `CurrentUser` 的 `-Scope` 時，必須具備適當的權限，才能建立或更新對應的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e788-135">When using a `-Scope` broader than `CurrentUser`, the appropriate permissions are required to create or update the corresponding profile file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e788-136">__只有__ Cmdlet 名稱會使用別名 - 模組名稱並不會。</span><span class="sxs-lookup"><span data-stu-id="4e788-136">__Only__ cmdlet names are aliased - module names aren't!</span></span> <span data-ttu-id="4e788-137">如果您使用 `#Requires`、`Import-Module`、`.psd1` 中的相依性清單，或完整的 Cmdlet 名稱，此時請確實依照[重大變更清單](migrate-az-1.0.0.md)中列出的模組名稱相關程序加以移轉。</span><span class="sxs-lookup"><span data-stu-id="4e788-137">If you're using `#Requires`, `Import-Module`, dependency lists in a `.psd1`, or fully-qualified cmdlet names, make sure that you migrate them at this point by following the process outlined in the [breaking changes list](migrate-az-1.0.0.md) regarding module names.</span></span>

> [!WARNING]
>
> <span data-ttu-id="4e788-138">您可以將不同的 `-Scope` 使用於這個命令，但不建議這麼做。</span><span class="sxs-lookup"><span data-stu-id="4e788-138">You can use a different `-Scope` for this command, but it's not recommended.</span></span> <span data-ttu-id="4e788-139">別名會寫入至所選範圍的使用者設定檔，所以儘可能在有限範圍內啟用別名。</span><span class="sxs-lookup"><span data-stu-id="4e788-139">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="4e788-140">全系統啟用別名，可能會對在其本機範圍內安裝 AzureRM 的其他使用者造成問題。</span><span class="sxs-lookup"><span data-stu-id="4e788-140">Enabling aliases system-wide can cause issues for other users who have AzureRM installed in their local scope.</span></span>

<span data-ttu-id="4e788-141">啟用別名模式後，再次執行指令碼以確認它們仍然運作正常。</span><span class="sxs-lookup"><span data-stu-id="4e788-141">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span>
<span data-ttu-id="4e788-142">Az 模組已變更、新增部分參數名稱，或將其設為必要項目。</span><span class="sxs-lookup"><span data-stu-id="4e788-142">Some parameter names have been changed, added, or made required by the Az module.</span></span> <span data-ttu-id="4e788-143">Cmdlet 的輸出類型也可能已變更。</span><span class="sxs-lookup"><span data-stu-id="4e788-143">Output types of cmdlets may have changed as well.</span></span> <span data-ttu-id="4e788-144">這些變更詳述於[重大變更清單](migrate-az-1.0.0.md)中。</span><span class="sxs-lookup"><span data-stu-id="4e788-144">These changes are detailed in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

## <a name="update-cmdlets-modules-and-parameters"></a><span data-ttu-id="4e788-145">更新 Cmdlet、模組和參數</span><span class="sxs-lookup"><span data-stu-id="4e788-145">Update cmdlets, modules, and parameters</span></span>

<span data-ttu-id="4e788-146">指令碼經過更新並以別名執行時，您可以妥善將其更新以使用新的 Cmdlet，並善用其他變更 (例如新功能)。</span><span class="sxs-lookup"><span data-stu-id="4e788-146">With scripts updated and running under aliases, you can take your time to update them to use the new cmdlets and take advantage of other changes like new features.</span></span> <span data-ttu-id="4e788-147">對於大部分的指令碼，您只需要[依照 Az 中新的 Cmdlet 命名配置](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes)更新 Cmdlet 名稱即可。</span><span class="sxs-lookup"><span data-stu-id="4e788-147">For most scripts, you will only need to update cmdlet names, [following the new cmdlet naming scheme in Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes).</span></span> <span data-ttu-id="4e788-148">您還可能需要進行其他某些變更，指令碼才能運作，視指令碼的功用及其運用的 Azure PowerShell 功能而定。</span><span class="sxs-lookup"><span data-stu-id="4e788-148">There may also be some other changes that you need to make in order to have your scripts work, depending on what they do and which Azure PowerShell features they take advantage of.</span></span>

<span data-ttu-id="4e788-149">例如，[Blob 儲存體 Cmdlet](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) 已完全重新撰寫而使用新的非同步模型，因此，相較於僅變更了 Cmdlet 名稱的指令碼，使用這類 Cmdlet 的指令碼將需要更多處理才能更新。</span><span class="sxs-lookup"><span data-stu-id="4e788-149">For example, the [Blob Storage cmdlets](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) have been completely reworked to use a new asynchronous model, so scripts using them will take more work to update than those where the only relevant changes were cmdlet names.</span></span>

<span data-ttu-id="4e788-150">即使您到目前為止只需要對指令碼進行簡單的微幅變更 (或者，您的指令碼在別名啟用時不需要進一步修改即可運作)，仍請參閱 [Az 1.0.0 中重大變更的完整清單](migrate-az-1.0.0.md)，以確定您並未依賴可能在您變更 Cmdlet 名稱和停用別名後即消失的「透明」別名行為。</span><span class="sxs-lookup"><span data-stu-id="4e788-150">Even if you've only had to make small, simple changes to your scripts up to this point - or they even work without additional modification when aliases are enabled -  read the [full list of breaking changes in Az 1.0.0](migrate-az-1.0.0.md) to make sure that you're not relying on 'transparent' behavior of aliases which could disappear after you change cmdlet names and disable aliases.</span></span>

## <a name="disable-aliases"></a><span data-ttu-id="4e788-151">停用別名</span><span class="sxs-lookup"><span data-stu-id="4e788-151">Disable aliases</span></span>

<span data-ttu-id="4e788-152">一旦您完成移轉，且不再依賴別名行為時，建議您停用別名。</span><span class="sxs-lookup"><span data-stu-id="4e788-152">Once you've completed your migration and are no longer relying on aliasing behavior, it's recommended that you disable aliases.</span></span> <span data-ttu-id="4e788-153">此作業可透過 [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) Cmdlet 來完成。</span><span class="sxs-lookup"><span data-stu-id="4e788-153">This is done with the [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e788-154">執行此 Cmdlet 時，請__確實__針對您已為其叫用 `Enable-AzureRmAlias` 的每個 `-Scope` 叫用 Cmdlet，否則您的系統上仍可能會有依賴別名行為的指令碼。</span><span class="sxs-lookup"><span data-stu-id="4e788-154">When running this cmdlet, __make sure__ that you invoke it for each `-Scope` that `Enable-AzureRmAlias` was invoked for, otherwise there may still be scripts on your system relying on the aliasing behavior.</span></span>
