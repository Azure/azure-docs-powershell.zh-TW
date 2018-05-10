---
title: 使用 Azure PowerShell 來登入
description: 使用 Azure PowerShell 來登入
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 1af5aeffb8e87e916df3e2440a84805935136c0f
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="87dac-103">使用 Azure PowerShell 來登入</span><span class="sxs-lookup"><span data-stu-id="87dac-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="87dac-104">Azure PowerShell 支援多種登入方法。</span><span class="sxs-lookup"><span data-stu-id="87dac-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="87dac-105">最簡單的入門方法是在命令列以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="87dac-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="87dac-106">互動式登入</span><span class="sxs-lookup"><span data-stu-id="87dac-106">Interactive log in</span></span>

1. <span data-ttu-id="87dac-107">輸入 `Login-AzureRmAccount`。</span><span class="sxs-lookup"><span data-stu-id="87dac-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="87dac-108">您會看到對話方塊，裡面會要求您提供 Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="87dac-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="87dac-109">輸入與您帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="87dac-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="87dac-110">Azure 會驗證並儲存認證資訊，然後關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="87dac-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="87dac-111">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="87dac-111">Log in with a service principal</span></span>

<span data-ttu-id="87dac-112">服務主體提供您建立非互動式帳戶的方式，以用來操控資源。</span><span class="sxs-lookup"><span data-stu-id="87dac-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="87dac-113">服務主體就像是使用者帳戶，您可以使用 Azure Active Directory 對其套用規則。</span><span class="sxs-lookup"><span data-stu-id="87dac-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="87dac-114">僅授與服務主體所需的最低權限，可確保您的自動化指令碼會更加安全。</span><span class="sxs-lookup"><span data-stu-id="87dac-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="87dac-115">如果您還沒有服務主體，請[建立一個](create-azure-service-principal-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="87dac-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="87dac-116">使用服務主體來登入。</span><span class="sxs-lookup"><span data-stu-id="87dac-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="87dac-117">若要取得您的 TenantId，請以互動方式登入，然後從您的訂用帳戶中取得 TenantId。</span><span class="sxs-lookup"><span data-stu-id="87dac-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

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

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="87dac-118">使用 Azure VM 受控服務識別登入</span><span class="sxs-lookup"><span data-stu-id="87dac-118">Log in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="87dac-119">受控服務識別 (MSI) 是 Azure Active Directory 的預覽功能。</span><span class="sxs-lookup"><span data-stu-id="87dac-119">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="87dac-120">您可以使用 MSI 服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。</span><span class="sxs-lookup"><span data-stu-id="87dac-120">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="87dac-121">如需 MSI 的詳細資訊，請參閱[如何使用 Azure VM 受控服務識別登入 (MSI) 進行登入和取得權杖](/azure/active-directory/msi-how-to-get-access-token-using-msi)。</span><span class="sxs-lookup"><span data-stu-id="87dac-121">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="87dac-122">登入其他雲端</span><span class="sxs-lookup"><span data-stu-id="87dac-122">Log in to another Cloud</span></span>

<span data-ttu-id="87dac-123">Azure 雲端服務提供不同的環境，以遵循各國政府的資料處理法規。</span><span class="sxs-lookup"><span data-stu-id="87dac-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="87dac-124">如果您的 Azure 帳戶位於某一個政府雲端，則需要在登入時指定環境。</span><span class="sxs-lookup"><span data-stu-id="87dac-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="87dac-125">例如，如果您的帳戶位於中國雲端，則可使用下列命令來登入：</span><span class="sxs-lookup"><span data-stu-id="87dac-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="87dac-126">使用下列命令來取得可用環境的清單：</span><span class="sxs-lookup"><span data-stu-id="87dac-126">Use the following command to get a list of available environments:</span></span>

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

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="87dac-127">深入了解如何管理 Azure 角色型存取</span><span class="sxs-lookup"><span data-stu-id="87dac-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="87dac-128">如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。</span><span class="sxs-lookup"><span data-stu-id="87dac-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="87dac-129">可用來管理角色的 Azure PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="87dac-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="87dac-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="87dac-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="87dac-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87dac-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="87dac-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="87dac-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="87dac-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87dac-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="87dac-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="87dac-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="87dac-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87dac-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="87dac-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87dac-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
