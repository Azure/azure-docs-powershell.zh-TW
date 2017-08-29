---
title: "使用 Azure PowerShell 來登入"
description: "使用 Azure PowerShell 來登入"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f6d249ca5bb09c4fe8445ba5b339ffa6012815ed
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/29/2017
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="ac459-103">使用 Azure PowerShell 來登入</span><span class="sxs-lookup"><span data-stu-id="ac459-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="ac459-104">Azure PowerShell 支援多種登入方法。</span><span class="sxs-lookup"><span data-stu-id="ac459-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="ac459-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="ac459-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="ac459-106">互動式登入</span><span class="sxs-lookup"><span data-stu-id="ac459-106">Interactive log in</span></span>

1. <span data-ttu-id="ac459-107">輸入 `Login-AzureRmAccount`。</span><span class="sxs-lookup"><span data-stu-id="ac459-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="ac459-108">您會看到對話方塊，裡面會要求您提供 Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="ac459-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="ac459-109">輸入與您帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="ac459-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="ac459-110">Azure 會驗證並儲存認證資訊，然後關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="ac459-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="ac459-111">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="ac459-111">Log in with a service principal</span></span>

<span data-ttu-id="ac459-112">服務主體提供您建立非互動式帳戶的方式，以用來操控資源。</span><span class="sxs-lookup"><span data-stu-id="ac459-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="ac459-113">服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。</span><span class="sxs-lookup"><span data-stu-id="ac459-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="ac459-114">僅授與服務主體所需的最低權限，可確保您的自動化指令碼會更加安全。</span><span class="sxs-lookup"><span data-stu-id="ac459-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="ac459-115">如果您還沒有服務主體，請[建立一個](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="ac459-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="ac459-116">使用服務主體來登入。</span><span class="sxs-lookup"><span data-stu-id="ac459-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="ac459-117">若要取得您的 TenantId，請以互動方式登入，然後從您的訂用帳戶中取得 TenantId。</span><span class="sxs-lookup"><span data-stu-id="ac459-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="ac459-118">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="ac459-118">Log in to another Cloud</span></span>

<span data-ttu-id="ac459-119">Azure 雲端服務提供不同的環境，以遵循各國政府的資料處理法規。</span><span class="sxs-lookup"><span data-stu-id="ac459-119">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="ac459-120">如果您的 Azure 帳戶位於某一個政府雲端，則需要在登入時指定環境。</span><span class="sxs-lookup"><span data-stu-id="ac459-120">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="ac459-121">例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：</span><span class="sxs-lookup"><span data-stu-id="ac459-121">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="ac459-122">使用下列命令來取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="ac459-122">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="ac459-123">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="ac459-123">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="ac459-124">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="ac459-124">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="ac459-125">可用來管理角色的 Azure PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac459-125">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="ac459-126">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ac459-126">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="ac459-127">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ac459-127">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="ac459-128">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ac459-128">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="ac459-129">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ac459-129">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="ac459-130">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ac459-130">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="ac459-131">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ac459-131">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="ac459-132">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ac459-132">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
