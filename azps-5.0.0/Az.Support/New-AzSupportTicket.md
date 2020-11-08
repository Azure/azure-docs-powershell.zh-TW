---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139902"
---
# <span data-ttu-id="11726-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="11726-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="11726-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11726-102">SYNOPSIS</span></span>
<span data-ttu-id="11726-103">建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-103">Creates a support ticket.</span></span>

## <span data-ttu-id="11726-104">句法</span><span class="sxs-lookup"><span data-stu-id="11726-104">SYNTAX</span></span>

### <span data-ttu-id="11726-105">CreateSupportTicketWithContactDetailParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11726-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11726-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11726-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11726-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11726-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11726-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11726-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11726-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="11726-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11726-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="11726-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11726-111">說明</span><span class="sxs-lookup"><span data-stu-id="11726-111">DESCRIPTION</span></span>
<span data-ttu-id="11726-112">這個 Cmdlet 可以用來建立帳單、訂閱管理、配額或技術問題的支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="11726-113">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification Cmdlet 來識別 Azure 服務，並分別針對您要要求支援的問題分類。</span><span class="sxs-lookup"><span data-stu-id="11726-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="11726-114">您必須指定下列參數：</span><span class="sxs-lookup"><span data-stu-id="11726-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="11726-115">您可以使用 New-AzSupportContactProfileObject helper Cmdlet 來建立 CustomerContactDetail 物件。</span><span class="sxs-lookup"><span data-stu-id="11726-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="11726-116">雲端解決方案提供者可以登入客戶的租使用者，並使用 *CSPHomeTenantId* 參數指定其家用租使用者識別碼，為其客戶的訂閱建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="11726-117">__針對技術入場券：__</span><span class="sxs-lookup"><span data-stu-id="11726-117">__For technical tickets:__</span></span>

<span data-ttu-id="11726-118">若要指定資源名稱，請使用 *TechnicalTicketResourceId* 參數來指定資源的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="11726-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="11726-119">請參閱下面的範例。</span><span class="sxs-lookup"><span data-stu-id="11726-119">See an example below.</span></span> 

<span data-ttu-id="11726-120">__針對配額票證：__</span><span class="sxs-lookup"><span data-stu-id="11726-120">__For quota tickets:__</span></span>

<span data-ttu-id="11726-121">若要針對 **計算 VM 核心** 、 **批次** **SQL 資料庫** 與 **SQL 資料倉儲** 要求配額增加，請在 [ *QuotaTicketDetail* 物件] 底下提供其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11726-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="11726-122">QuotaTicketDetail 物件由3個屬性組成，如下所述。</span><span class="sxs-lookup"><span data-stu-id="11726-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="11726-123">如需詳細檔，請 [按一下這裡。](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="11726-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

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


<span data-ttu-id="11726-124">如需如何針對各種配額類型構造負載的詳細檔，請 [按一下這裡](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="11726-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="11726-125">示例</span><span class="sxs-lookup"><span data-stu-id="11726-125">EXAMPLES</span></span>

### <span data-ttu-id="11726-126">範例1：建立帳單或訂閱管理支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="11726-127">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification 來針對您要要求支援的計費或訂閱管理問題分類來檢索正確的 Guid</span><span class="sxs-lookup"><span data-stu-id="11726-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-128">範例2：建立適用于 Windows 資源的虛擬機器的技術支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="11726-129">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification 來檢索 Windows 版虛擬機器的正確 Guid，以取得您要要求支援的分類問題分類</span><span class="sxs-lookup"><span data-stu-id="11726-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-130">範例3：建立配額支援票證以增加特定 VM 系列的虛擬電腦核心配額。</span><span class="sxs-lookup"><span data-stu-id="11726-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="11726-131">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額計算 VM 核心問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-132">範例4：建立配額支援票證，以增加 Batch 帳戶低優先順序核心的配額。</span><span class="sxs-lookup"><span data-stu-id="11726-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="11726-133">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額批次問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-134">範例5：建立配額支援票證，以增加批次帳戶特定 VM 系列的 VM 核心配額。</span><span class="sxs-lookup"><span data-stu-id="11726-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="11726-135">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額批次問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-136">範例6：建立配額支援票證以增加 Batch 帳戶的 Pool quota。</span><span class="sxs-lookup"><span data-stu-id="11726-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="11726-137">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額批次問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-138">範例7：建立配額支援票證以增加批次帳戶的作用中作業與作業排程配額。</span><span class="sxs-lookup"><span data-stu-id="11726-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="11726-139">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額批次問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-140">範例8：建立配額支援票證以增加訂閱的批次帳戶數目。</span><span class="sxs-lookup"><span data-stu-id="11726-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="11726-141">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額批次問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-142">範例9：建立配額支援票證，以增加 SQL 資料庫 Dtu 的配額。</span><span class="sxs-lookup"><span data-stu-id="11726-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="11726-143">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額 SQL 資料庫問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-144">範例10：建立配額支援票證以增加 SQL 資料庫伺服器的配額。</span><span class="sxs-lookup"><span data-stu-id="11726-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="11726-145">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額 SQL 資料庫問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-146">範例11：建立配額支援票證，以增加 SQL 資料倉儲的 Dtu 配額。</span><span class="sxs-lookup"><span data-stu-id="11726-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="11726-147">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額 SQL 日期倉庫問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-148">範例12：建立配額支援票證以增加 SQL 資料倉儲的伺服器配額。</span><span class="sxs-lookup"><span data-stu-id="11726-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="11726-149">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification，以針對配額 SQL 資料倉儲問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-150">範例13：建立配額支援票證，以增加電腦學習服務低優先順序核心的配額。</span><span class="sxs-lookup"><span data-stu-id="11726-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="11726-151">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification 來為配額機器學習服務問題分類取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-152">範例14：建立配額支援票證，為電腦學習服務的特定 VM 系列增加 VM 核心配額。</span><span class="sxs-lookup"><span data-stu-id="11726-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="11726-153">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification 來為配額機器學習服務問題分類取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-154">範例15：建立配額支援票證以增加 Azure SQL Managed 實例的配額。</span><span class="sxs-lookup"><span data-stu-id="11726-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="11726-155">使用 Get-AzSupportService 和 Get-AzSupportProblemClassification 來針對配額 SQL Managed 實例服務問題分類來取得正確的 Guid。</span><span class="sxs-lookup"><span data-stu-id="11726-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-156">範例16：指定個別客戶連絡人參數（而非 CustomerContactDetail 物件），以建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-157">範例17：建立支援票證，並要求來自 Azure 的 24 x 7 回應。</span><span class="sxs-lookup"><span data-stu-id="11726-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="11726-158">範例18：如果您是雲端解決方案提供者 (CSP) ，請代表您的客戶建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="11726-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="11726-159">CSP 應該先登入其租使用者，然後登入客戶的租使用者，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="11726-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="11726-160">然後，必須使用-CSPHomeTenantId 參數來指定其在建立支援票證時的主租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="11726-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="11726-161">參數</span><span class="sxs-lookup"><span data-stu-id="11726-161">PARAMETERS</span></span>

### <span data-ttu-id="11726-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="11726-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="11726-163">其他電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="11726-163">Additional email addresses.</span></span>
<span data-ttu-id="11726-164">此處列出的電子郵件地址將會在有關支援票證的任何函件上複製。</span><span class="sxs-lookup"><span data-stu-id="11726-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="11726-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11726-165">-AsJob</span></span>
<span data-ttu-id="11726-166">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11726-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="11726-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="11726-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="11726-168">這是用來嘗試為客戶建立支援票證之雲端解決方案提供者的「家用租使用者識別碼」。</span><span class="sxs-lookup"><span data-stu-id="11726-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="11726-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="11726-169">-CustomerContactDetail</span></span>
<span data-ttu-id="11726-170">與 SupportTicket 資源相關聯的客戶連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11726-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="11726-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="11726-171">-CustomerCountry</span></span>
<span data-ttu-id="11726-172">客戶國家/地區。</span><span class="sxs-lookup"><span data-stu-id="11726-172">Customer country.</span></span>
<span data-ttu-id="11726-173">這必須是合法的 ISO Alpha-3 國家/地區代碼 (ISO 3166) 。</span><span class="sxs-lookup"><span data-stu-id="11726-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="11726-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="11726-174">-CustomerFirstName</span></span>
<span data-ttu-id="11726-175">客戶名字。</span><span class="sxs-lookup"><span data-stu-id="11726-175">Customer first name.</span></span>

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

### <span data-ttu-id="11726-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="11726-176">-CustomerLastName</span></span>
<span data-ttu-id="11726-177">客戶姓氏。</span><span class="sxs-lookup"><span data-stu-id="11726-177">Customer last name.</span></span>

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

### <span data-ttu-id="11726-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="11726-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="11726-179">客戶電話號碼。</span><span class="sxs-lookup"><span data-stu-id="11726-179">Customer phone number.</span></span>
<span data-ttu-id="11726-180">如果您喜歡的連絡方式是手機，則需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="11726-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="11726-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="11726-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="11726-182">自訂的 Peferred 語言。</span><span class="sxs-lookup"><span data-stu-id="11726-182">Peferred language of the custom.</span></span>
<span data-ttu-id="11726-183">這必須是有效的語言 contry 程式碼，適用于此處所列的其中一個支援的語言 https://azure.microsoft.com/en-us/support/faq/ 。</span><span class="sxs-lookup"><span data-stu-id="11726-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="11726-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="11726-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="11726-185">客戶慣用時區。</span><span class="sxs-lookup"><span data-stu-id="11726-185">Customer preferred time zone.</span></span>
<span data-ttu-id="11726-186">這必須是有效的 System.TimeZoneInfo.Id 值。</span><span class="sxs-lookup"><span data-stu-id="11726-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="11726-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="11726-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="11726-188">客戶主要電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="11726-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="11726-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11726-189">-DefaultProfile</span></span>
<span data-ttu-id="11726-190">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11726-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11726-191">-描述</span><span class="sxs-lookup"><span data-stu-id="11726-191">-Description</span></span>
<span data-ttu-id="11726-192">問題或問題的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="11726-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="11726-193">-名稱</span><span class="sxs-lookup"><span data-stu-id="11726-193">-Name</span></span>
<span data-ttu-id="11726-194">此 Cmdlet 建立的支援票證的名稱。</span><span class="sxs-lookup"><span data-stu-id="11726-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11726-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="11726-195">-PreferredContactMethod</span></span>
<span data-ttu-id="11726-196">[首選連絡方式] 方法。</span><span class="sxs-lookup"><span data-stu-id="11726-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="11726-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="11726-197">-ProblemClassificationId</span></span>
<span data-ttu-id="11726-198">每個 Azure 服務都有自己的一組問題類別，名為「問題分類」，且與您所遇到的問題類型相對應。</span><span class="sxs-lookup"><span data-stu-id="11726-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="11726-199">這個參數是 ProblemClassification 資源的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="11726-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="11726-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="11726-200">-ProblemStartTime</span></span>
<span data-ttu-id="11726-201">問題開始的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="11726-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="11726-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="11726-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="11726-203">配額支援票證的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11726-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="11726-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="11726-204">-Require24X7Response</span></span>
<span data-ttu-id="11726-205">指出此支援票證是否需要從 Azure 進行全天候回應。</span><span class="sxs-lookup"><span data-stu-id="11726-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="11726-206">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="11726-206">-Severity</span></span>
<span data-ttu-id="11726-207">支援票證的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="11726-207">Severity of the support ticket.</span></span>
<span data-ttu-id="11726-208">這會指出案例的緊急性，然後根據您所擁有的 Azure 技術支援方案服務層級合約來判斷回應時間。</span><span class="sxs-lookup"><span data-stu-id="11726-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="11726-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="11726-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="11726-210">這是 Azure 服務資源 (的資源識別碼，例如：建立支援票證的虛擬機器資源或 HDInsight 資源) 。</span><span class="sxs-lookup"><span data-stu-id="11726-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="11726-211">-標題</span><span class="sxs-lookup"><span data-stu-id="11726-211">-Title</span></span>
<span data-ttu-id="11726-212">支援票證的標題。</span><span class="sxs-lookup"><span data-stu-id="11726-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="11726-213">-確認</span><span class="sxs-lookup"><span data-stu-id="11726-213">-Confirm</span></span>
<span data-ttu-id="11726-214">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11726-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11726-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11726-215">-WhatIf</span></span>
<span data-ttu-id="11726-216">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11726-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11726-217">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11726-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11726-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11726-218">CommonParameters</span></span>
<span data-ttu-id="11726-219">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11726-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11726-220">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11726-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11726-221">輸入</span><span class="sxs-lookup"><span data-stu-id="11726-221">INPUTS</span></span>

### <span data-ttu-id="11726-222">所有</span><span class="sxs-lookup"><span data-stu-id="11726-222">None</span></span>

## <span data-ttu-id="11726-223">輸出</span><span class="sxs-lookup"><span data-stu-id="11726-223">OUTPUTS</span></span>

### <span data-ttu-id="11726-224">PSSupportTicket （支援）。</span><span class="sxs-lookup"><span data-stu-id="11726-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="11726-225">筆記</span><span class="sxs-lookup"><span data-stu-id="11726-225">NOTES</span></span>

## <span data-ttu-id="11726-226">相關連結</span><span class="sxs-lookup"><span data-stu-id="11726-226">RELATED LINKS</span></span>
