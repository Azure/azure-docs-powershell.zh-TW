---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 0d86d4e01c39170975901f5c9262bc2857883eec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907030"
---
# <span data-ttu-id="d7148-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="d7148-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="d7148-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7148-102">SYNOPSIS</span></span>
<span data-ttu-id="d7148-103">建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="d7148-103">Creates a support ticket.</span></span>

## <span data-ttu-id="d7148-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7148-104">SYNTAX</span></span>

### <span data-ttu-id="d7148-105">CreateSupportTicketWithContactDetailParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d7148-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7148-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7148-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7148-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7148-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7148-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7148-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7148-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7148-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7148-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7148-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7148-111">描述</span><span class="sxs-lookup"><span data-stu-id="d7148-111">DESCRIPTION</span></span>
<span data-ttu-id="d7148-112">此 Cmdlet 可用來建立帳單、訂閱管理、配額或技術問題的支援票證。</span><span class="sxs-lookup"><span data-stu-id="d7148-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="d7148-113">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification Cmdlet 來識別 Azure 服務，以及要要求支援的對應問題分類。</span><span class="sxs-lookup"><span data-stu-id="d7148-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="d7148-114">您必須指定下列參數：</span><span class="sxs-lookup"><span data-stu-id="d7148-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="d7148-115">您可以使用 New-AzSupportContactProfileObject Cmdlet 來建立 CustomerContactDetail 物件。</span><span class="sxs-lookup"><span data-stu-id="d7148-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="d7148-116">雲端解決方案提供者可以登入客戶的租使用者，然後使用 *CSPHomeTenantId* 參數指定其家庭租使用者識別碼，以建立客戶訂閱的支援票證。</span><span class="sxs-lookup"><span data-stu-id="d7148-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="d7148-117">__對於技術票證：__</span><span class="sxs-lookup"><span data-stu-id="d7148-117">__For technical tickets:__</span></span>

<span data-ttu-id="d7148-118">若要指定資源名稱，請用 *TechnicalTicketResourceId* 參數指定資源的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7148-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="d7148-119">請參閱下列範例。</span><span class="sxs-lookup"><span data-stu-id="d7148-119">See an example below.</span></span> 

<span data-ttu-id="d7148-120">__對於配額票證：__</span><span class="sxs-lookup"><span data-stu-id="d7148-120">__For quota tickets:__</span></span>

<span data-ttu-id="d7148-121">若要要求增加 Compute **VM Cores、Batch、SQL** **Database** 和 **SQL Data Warehouse** 的配額，請提供 *QuotaTicketDetail* 物件下的其他詳細資料。 </span><span class="sxs-lookup"><span data-stu-id="d7148-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="d7148-122">QuotaTicketDetail 物件包含 3 個屬性，如下所述。</span><span class="sxs-lookup"><span data-stu-id="d7148-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="d7148-123">如需詳細檔， [請按一下這裡。](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="d7148-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="d7148-124">如需如何建構各種配額類型之有效負載的詳細檔， [請按一下這裡](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="d7148-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="d7148-125">例子</span><span class="sxs-lookup"><span data-stu-id="d7148-125">EXAMPLES</span></span>

### <span data-ttu-id="d7148-126">範例 1：建立帳單或訂閱管理支援票證。</span><span class="sxs-lookup"><span data-stu-id="d7148-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="d7148-127">使用Get-AzSupportServiceGet-AzSupportProblemClassification以針對帳單或訂閱管理問題分類，針對您想要要求支援的正確 GUID</span><span class="sxs-lookup"><span data-stu-id="d7148-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-128">範例 2：為 Windows 虛擬機器資源建立技術支援票證。</span><span class="sxs-lookup"><span data-stu-id="d7148-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="d7148-129">使用Get-AzSupportServiceGet-AzSupportProblemClassification來針對 Windows 虛擬機器問題分類，以要求支援的正確 GUID</span><span class="sxs-lookup"><span data-stu-id="d7148-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-130">範例 3：建立配額支援票證，以增加特定 VM 系列虛擬機器核心機的配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="d7148-131">使用Get-AzSupportServiceGet-AzSupportProblemClassification以針對配額計算 VM 核心機問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-132">範例 4：建立配額支援票證，增加批次帳戶低優先順序核心的配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="d7148-133">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額批次問題分類來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-134">範例 5：建立配額支援票證，增加批次帳戶的特定 VM 系列之 VM 核心配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="d7148-135">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額批次問題分類來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-136">範例 6：建立配額支援票證以增加批次帳戶的資料庫配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="d7148-137">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額批次問題分類來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-138">範例 7：建立配額支援票證，增加批次帳戶的活動工作與工作排程配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="d7148-139">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額批次問題分類來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-140">範例 8：建立配額支援票證以增加訂閱的批次帳戶數目。</span><span class="sxs-lookup"><span data-stu-id="d7148-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="d7148-141">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額批次問題分類來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-142">範例 9：建立配額支援票證以增加 SQL Database 的 DTUs 配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="d7148-143">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額 SQL 資料庫問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-144">範例 10：建立配額支援票證來增加 SQL Database Server 的配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="d7148-145">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額 SQL 資料庫問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-146">範例 11：建立配額支援票證以增加 SQL Data Warehouse 的 DTUs 配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="d7148-147">使用Get-AzSupportService和Get-AzSupportProblemClassification以針對配額 SQL 日期倉庫問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-148">範例 12：建立配額支援票證以增加 SQL Data Warehouse 伺服器配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="d7148-149">使用Get-AzSupportService和Get-AzSupportProblemClassification以針對配額 SQL 資料倉儲問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-150">範例 13：建立配額支援票證以增加機器學習服務低優先順序核心的配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="d7148-151">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額機器學習服務問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-152">範例 14：建立配額支援票證以增加特定 VM 家用電腦學習服務之 VM 核心配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="d7148-153">使用Get-AzSupportService和Get-AzSupportProblemClassification來針對配額機器學習服務問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-154">範例 15：建立配額支援票證以增加 Azure SQL Managed 實例的配額。</span><span class="sxs-lookup"><span data-stu-id="d7148-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="d7148-155">使用Get-AzSupportService和Get-AzSupportProblemClassification以針對配額 SQL Managed Instance 服務問題分類，來取回正確的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7148-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-156">範例 16：指定個別的客戶連絡人參數，而不是 CustomerContactDetail 物件，以建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="d7148-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-157">範例 17：建立支援票證，並要求 Azure 24 x 7 回應。</span><span class="sxs-lookup"><span data-stu-id="d7148-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="d7148-158">範例 18：如果您是雲端解決方案提供者或雲端解決方案提供者雲端解決方案提供者，請代表您的客戶 (支援) 。</span><span class="sxs-lookup"><span data-stu-id="d7148-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="d7148-159">CSP 應該先登入其租使用者，然後登入客戶的租使用者，如以下範例所示。</span><span class="sxs-lookup"><span data-stu-id="d7148-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="d7148-160">他們接著必須使用 -CSPHomeTenantId 參數，在建立支援票證時指定其家庭租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7148-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="d7148-161">參數</span><span class="sxs-lookup"><span data-stu-id="d7148-161">PARAMETERS</span></span>

### <span data-ttu-id="d7148-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d7148-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="d7148-163">其他電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="d7148-163">Additional email addresses.</span></span>
<span data-ttu-id="d7148-164">此處所列的電子郵件地址將會複製到支援票證的任何對應。</span><span class="sxs-lookup"><span data-stu-id="d7148-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7148-165">-AsJob</span></span>
<span data-ttu-id="d7148-166">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7148-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="d7148-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="d7148-168">這是雲端解決方案提供者使用者嘗試為客戶建立支援票證的家用租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7148-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="d7148-169">-CustomerContactDetail</span></span>
<span data-ttu-id="d7148-170">與 SupportTicket 資源相關聯的客戶連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d7148-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="d7148-171">-CustomerCountry</span></span>
<span data-ttu-id="d7148-172">客戶國家/地區。</span><span class="sxs-lookup"><span data-stu-id="d7148-172">Customer country.</span></span>
<span data-ttu-id="d7148-173">這必須是 ISO 3166 (有效的 ISO Alpha-3) 。</span><span class="sxs-lookup"><span data-stu-id="d7148-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="d7148-174">-CustomerFirstName</span></span>
<span data-ttu-id="d7148-175">客戶名字。</span><span class="sxs-lookup"><span data-stu-id="d7148-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="d7148-176">-CustomerLastName</span></span>
<span data-ttu-id="d7148-177">客戶姓氏。</span><span class="sxs-lookup"><span data-stu-id="d7148-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d7148-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="d7148-179">客戶電話號碼。</span><span class="sxs-lookup"><span data-stu-id="d7148-179">Customer phone number.</span></span>
<span data-ttu-id="d7148-180">如果偏好的連絡人方法是電話，則此為必填專案。</span><span class="sxs-lookup"><span data-stu-id="d7148-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="d7148-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="d7148-182">自訂的推斷語言。</span><span class="sxs-lookup"><span data-stu-id="d7148-182">Peferred language of the custom.</span></span>
<span data-ttu-id="d7148-183">這必須是此處所列的其中一個支援語言的有效語言代碼 https://azure.microsoft.com/en-us/support/faq/ 。</span><span class="sxs-lookup"><span data-stu-id="d7148-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="d7148-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="d7148-185">客戶偏好的時區。</span><span class="sxs-lookup"><span data-stu-id="d7148-185">Customer preferred time zone.</span></span>
<span data-ttu-id="d7148-186">這必須是有效的System.TimeZoneInfo.Id值。</span><span class="sxs-lookup"><span data-stu-id="d7148-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d7148-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="d7148-188">客戶主要電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="d7148-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7148-189">-DefaultProfile</span></span>
<span data-ttu-id="d7148-190">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7148-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-191">-描述</span><span class="sxs-lookup"><span data-stu-id="d7148-191">-Description</span></span>
<span data-ttu-id="d7148-192">問題或問題的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="d7148-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-193">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7148-193">-Name</span></span>
<span data-ttu-id="d7148-194">此 Cmdlet 建立的支援票證名稱。</span><span class="sxs-lookup"><span data-stu-id="d7148-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="d7148-195">-PreferredContactMethod</span></span>
<span data-ttu-id="d7148-196">偏好的連絡人方法。</span><span class="sxs-lookup"><span data-stu-id="d7148-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="d7148-197">-ProblemClassificationId</span></span>
<span data-ttu-id="d7148-198">每個 Azure 服務都有自己的問題類別，稱為問題分類，對應到您遇到的問題類型。</span><span class="sxs-lookup"><span data-stu-id="d7148-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="d7148-199">此參數是 ProblemClassification 資源的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7148-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-200">-問題啟動時間</span><span class="sxs-lookup"><span data-stu-id="d7148-200">-ProblemStartTime</span></span>
<span data-ttu-id="d7148-201">發生問題的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d7148-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="d7148-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="d7148-203">配額支援票證的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d7148-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="d7148-204">-Require24X7Response</span></span>
<span data-ttu-id="d7148-205">指出此支援票證是否需要來自 Azure 的 24x7 回應。</span><span class="sxs-lookup"><span data-stu-id="d7148-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-206">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="d7148-206">-Severity</span></span>
<span data-ttu-id="d7148-207">支援票證的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="d7148-207">Severity of the support ticket.</span></span>
<span data-ttu-id="d7148-208">這表示案例的緊急性，進而會依據您與 Azure 之技術支援方案的服務等級協定決定回應時間。</span><span class="sxs-lookup"><span data-stu-id="d7148-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="d7148-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="d7148-210">這是 Azure 服務資源的資源識別碼 (例如：建立支援票證的虛擬機器資源或 HDInsight) 。</span><span class="sxs-lookup"><span data-stu-id="d7148-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-211">-標題</span><span class="sxs-lookup"><span data-stu-id="d7148-211">-Title</span></span>
<span data-ttu-id="d7148-212">支援票證的標題。</span><span class="sxs-lookup"><span data-stu-id="d7148-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-213">-確認</span><span class="sxs-lookup"><span data-stu-id="d7148-213">-Confirm</span></span>
<span data-ttu-id="d7148-214">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d7148-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7148-215">-WhatIf</span></span>
<span data-ttu-id="d7148-216">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7148-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7148-217">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7148-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7148-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7148-218">CommonParameters</span></span>
<span data-ttu-id="d7148-219">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7148-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7148-220">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7148-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7148-221">輸入</span><span class="sxs-lookup"><span data-stu-id="d7148-221">INPUTS</span></span>

### <span data-ttu-id="d7148-222">沒有</span><span class="sxs-lookup"><span data-stu-id="d7148-222">None</span></span>

## <span data-ttu-id="d7148-223">輸出</span><span class="sxs-lookup"><span data-stu-id="d7148-223">OUTPUTS</span></span>

### <span data-ttu-id="d7148-224">Microsoft.Azure.Commands.support.models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="d7148-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="d7148-225">筆記</span><span class="sxs-lookup"><span data-stu-id="d7148-225">NOTES</span></span>

## <span data-ttu-id="d7148-226">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7148-226">RELATED LINKS</span></span>
