---
title: Azure 內容和登入認證
description: 了解如何重覆使用 Azure 認證及多個 PowerShell 工作階段之間的其他資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: c79d1d634d5b76b2c6ab6b6ab309c2d49f9f7678
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2020
ms.locfileid: "84299395"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="e0f6d-103">Azure PowerShell 內容物件</span><span class="sxs-lookup"><span data-stu-id="e0f6d-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="e0f6d-104">Azure PowerShell 會使用 _Azure PowerShell 內容物件_ (Azure 內容) 來保存訂用帳戶和驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="e0f6d-105">如果您有多個訂用帳戶，Azure 內容可讓您選取要執行 Azure PowerShell Cmdlet 的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="e0f6d-106">Azure 內容也可用來跨多個 PowerShell 工作階段儲存登入資訊，以及執行背景工作。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="e0f6d-107">本文將說明如何管理 Azure 內容，而非管理訂用帳戶或帳戶。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="e0f6d-108">如果您想要管理使用者、訂用帳戶、租用戶或其他帳戶資訊，請參閱 [Azure Active Directory](/azure/active-directory) 文件。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="e0f6d-109">若要了解如何使用內容來執行背景或平行工作，請在熟悉 Azure 內容後，參閱[在 PowerShell 作業中使用 Azure PowerShell Cmdlet](using-psjobs.md)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="e0f6d-110">Azure 內容物件概觀</span><span class="sxs-lookup"><span data-stu-id="e0f6d-110">Overview of Azure context objects</span></span>

<span data-ttu-id="e0f6d-111">Azure 內容是 PowerShell 物件，代表您對其執行命令的有效訂用帳戶，以及連線至 Azure 雲端所需的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="e0f6d-112">透過 Azure 內容，Azure PowerShell 就不需要在您每次切換訂用帳戶時重新驗證您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="e0f6d-113">Azure 內容包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-113">An Azure context consists of:</span></span>

* <span data-ttu-id="e0f6d-114">用來透過 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) 登入 Azure 的_帳戶_。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="e0f6d-115">就帳戶的觀點而言，Azure 內容會將使用者、應用程式識別碼和服務主體等同視之。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="e0f6d-116">有效_訂用帳戶_是 Microsoft 提供的服務合約，用來建立和執行與_租用戶_相關聯的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="e0f6d-117">租用戶在文件中或使用 Active Directory 時，通常稱為_組織_。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="e0f6d-118">_權杖快取_的參考是用來存取 Azure 雲端的預存驗證權杖。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="e0f6d-119">此權杖的儲存位置及其保存的時間長度，取決於[內容自動儲存設定](#save-azure-contexts-across-powershell-sessions)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="e0f6d-120">如需這些字詞的詳細資訊，請參閱 [Azure Active Directory 術語](/azure/active-directory/fundamentals/active-directory-whatis#terminology)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="e0f6d-121">Azure 內容所使用的驗證權杖與持續性工作階段中其他已儲存的權杖相同。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="e0f6d-122">當您使用 `Connect-AzAccount` 登入時，系統會為您的預設訂用帳戶建立至少一個 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="e0f6d-123">`Connect-AzAccount` 傳回的物件是預設的 Azure 內容，用於其餘的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="e0f6d-124">取得 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="e0f6d-124">Get Azure contexts</span></span>

<span data-ttu-id="e0f6d-125">可用的 Azure 內容可使用 [Get-AzContext](/powershell/module/az.accounts/get-azcontext) Cmdlet 來擷取。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="e0f6d-126">您可以使用 `-ListAvailable` 列出所有可用的內容：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="e0f6d-127">或依名稱取得內容：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="e0f6d-128">內容名稱可能與相關聯的訂用帳戶名稱不同。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0f6d-129">可用的 Azure 內容__不一定__是您可用的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="e0f6d-130">Azure 內容僅代表本機儲存的資訊。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="e0f6d-131">您可以使用 [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) Cmdlet 取得訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="e0f6d-132">從訂用帳戶資訊建立新的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="e0f6d-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="e0f6d-133">[Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) Cmdlet 可用來建立新的 Azure 內容，並將其設定為有效內容。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="e0f6d-134">要建立新的 Azure 內容，最簡單的方式是使用現有的訂用帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="e0f6d-135">此 Cmdlet 依設計會使用 `Get-AzSubscription` 的輸出物件作為管線值，並設定新的 Azure 內容：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="e0f6d-136">或者，視需要提供訂用帳戶名稱或識別碼和租用戶識別碼：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="e0f6d-137">如果省略 `-Name` 引數，則會以訂用帳戶的名稱和識別碼作為 `Subscription Name (subscription-id)` 格式的內容名稱。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="e0f6d-138">變更有效的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="e0f6d-138">Change the active Azure context</span></span>

<span data-ttu-id="e0f6d-139">`Set-AzContext` 和 [Select-AzContext](/powershell/module/az.accounts/set-azcontext) 都可用來變更有效的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="e0f6d-140">如[建立新的 Azure 內容](#create-a-new-azure-context-from-subscription-information)中所說明，`Set-AzContext` 會為訂用帳戶建立新的 Azure 內容 (如果沒有的話)，然後切換為以該內容作為有效內容。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="e0f6d-141">`Select-AzContext` 僅適用於現有的 Azure 內容，且其運作方式與使用 `Set-AzContext -Context` 時類似，但正規用途為管線輸送：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="e0f6d-142">如同 Azure PowerShell 中的許多其他帳戶和內容管理命令，`Set-AzContext` 和 `Select-AzContext` 均支援 `-Scope` 引數，讓您可以控制內容的有效期間。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="e0f6d-143">`-Scope` 可讓您直接變更單一工作階段的有效內容，而無須變更預設值：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="e0f6d-144">若要避免切換整個 PowerShell 工作階段的內容，您可以使用 `-AzContext` 引數對指定內容執行所有的 Azure PowerShell 命令：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="e0f6d-145">以 Azure PowerShell Cmdlet 處理內容的另一項主要用途，是執行背景命令。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="e0f6d-146">若要深入了解如何使用 Azure PowerShell 執行 PowerShell 作業，請參閱[在 PowerShell 作業中執行 Azure PowerShell Cmdlet](using-psjobs.md)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="e0f6d-147">跨 PowerShell 工作階段儲存 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="e0f6d-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="e0f6d-148">根據預設，Azure 內容會儲存起來以在 PowerShell 工作階段之間使用。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="e0f6d-149">您可以透過下列方式變更此行為︰</span><span class="sxs-lookup"><span data-stu-id="e0f6d-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="e0f6d-150">搭配使用 `-Scope Process` 與 `Connect-AzAccount` 登入。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="e0f6d-151">在此登入的過程中傳回的 Azure 內容，有效性_僅_及於目前的工作階段，且無論 Azure PowerShell 內容自動儲存設定為何，都不會自動儲存。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="e0f6d-152">使用 [Disable-AzCoNtextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) Cmdlet 將 AzurePowershell 的內容自動儲存停用。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="e0f6d-153">停用內容自動儲存並__不會__清除任何已儲存的權杖。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="e0f6d-154">若要了解如何清除已儲存的 Azure 內容資訊，請參閱[移除 Azure 內容和認證](#remove-azure-contexts-and-stored-credentials)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="e0f6d-155">若要明確啟用 Azure 內容自動儲存，可以使用 [Enable-AzCoNtextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) Cmdlet 來啟用。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="e0f6d-156">自動儲存啟用時，所有使用者內容都會儲存在本機，以供後續的 PowerShell 工作階段使用。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="e0f6d-157">使用 [Save-AzContext](/powershell/module/az.accounts/save-azcontext) 手動儲存內容以供未來的 PowerShell 工作階段使用，並可在 [Import-AzContext](/powershell/module/az.accounts/import-azcontext) 來載入：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="e0f6d-158">停用內容自動儲存並__不會__清除任何已儲存的預存內容資訊。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="e0f6d-159">若要移除已儲存的資訊，請使用 [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="e0f6d-160">如需移除已儲存內容的詳細資訊，請參閱[移除內容和認證](#remove-azure-contexts-and-stored-credentials)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="e0f6d-161">前述每個命令都支援 `-Scope` 參數，此參數可使用 `Process` 值而僅套用至目前執行中的程序。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="e0f6d-162">例如，若要確保在結束 PowerShell 工作階段之後不會儲存新建立的內容：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="e0f6d-163">內容資訊和權杖都會儲存在 Windows 上的 `$env:USERPROFILE\.Azure` 目錄中，以及其他平台的 `$HOME/.Azure` 中。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="e0f6d-164">敏感性資訊 (例如訂用帳戶識別碼和租用戶識別碼) 可能仍會透過記錄或已儲存的內容公開於已儲存的資訊中。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="e0f6d-165">若要了解如何清除已儲存的資訊，請參閱[移除內容和認證](#remove-azure-contexts-and-stored-credentials)一節。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="e0f6d-166">移除 Azure 內容和已儲存的認證</span><span class="sxs-lookup"><span data-stu-id="e0f6d-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="e0f6d-167">若要清除 Azure 內容和認證：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="e0f6d-168">使用 [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) 登出帳戶。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="e0f6d-169">您可以透過帳戶或內容登出任何帳戶：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="e0f6d-170">中斷連線後一律會移除已儲存的驗證權杖，並清除與中斷連線的使用者或內容相關聯的已儲存內容。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="e0f6d-171">使用 [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext)。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="e0f6d-172">此 Cmdlet 一律會移除已儲存的內容和驗證權杖，而且也會將您登出。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="e0f6d-173">使用 [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) 移除內容：</span><span class="sxs-lookup"><span data-stu-id="e0f6d-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="e0f6d-174">如果您移除有效內容，您將會與 Azure 中斷連線，而需要使用 `Connect-AzAccount` 重新進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e0f6d-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0f6d-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0f6d-175">See also</span></span>

* [<span data-ttu-id="e0f6d-176">在 PowerShell 作業中執行 Azure PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e0f6d-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="e0f6d-177">Azure Active Directory 術語</span><span class="sxs-lookup"><span data-stu-id="e0f6d-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="e0f6d-178">Az.Accounts 參考</span><span class="sxs-lookup"><span data-stu-id="e0f6d-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
