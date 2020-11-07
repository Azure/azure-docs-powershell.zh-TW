---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794889"
---
# <span data-ttu-id="5d36a-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="5d36a-101">Close-AzsAlert</span></span>

## <span data-ttu-id="5d36a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d36a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d36a-103">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="5d36a-103">Closes the given alert.</span></span>

## <span data-ttu-id="5d36a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d36a-104">SYNTAX</span></span>

### <span data-ttu-id="5d36a-105">CloseExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5d36a-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d36a-106">結轉</span><span class="sxs-lookup"><span data-stu-id="5d36a-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d36a-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d36a-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d36a-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5d36a-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d36a-109">說明</span><span class="sxs-lookup"><span data-stu-id="5d36a-109">DESCRIPTION</span></span>
<span data-ttu-id="5d36a-110">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="5d36a-110">Closes the given alert.</span></span>

## <span data-ttu-id="5d36a-111">示例</span><span class="sxs-lookup"><span data-stu-id="5d36a-111">EXAMPLES</span></span>

### <span data-ttu-id="5d36a-112">範例1：</span><span class="sxs-lookup"><span data-stu-id="5d36a-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="5d36a-113">依名稱關閉警示。</span><span class="sxs-lookup"><span data-stu-id="5d36a-113">Close an alert by Name.</span></span>

### <span data-ttu-id="5d36a-114">範例2：</span><span class="sxs-lookup"><span data-stu-id="5d36a-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="5d36a-115">透過 [管道] 關閉警示。</span><span class="sxs-lookup"><span data-stu-id="5d36a-115">Close an alert through piping.</span></span>

## <span data-ttu-id="5d36a-116">參數</span><span class="sxs-lookup"><span data-stu-id="5d36a-116">PARAMETERS</span></span>

### <span data-ttu-id="5d36a-117">-提醒</span><span class="sxs-lookup"><span data-stu-id="5d36a-117">-Alert</span></span>
<span data-ttu-id="5d36a-118">這個物件代表警示資源。</span><span class="sxs-lookup"><span data-stu-id="5d36a-118">This object represents an alert resource.</span></span>
<span data-ttu-id="5d36a-119">若要建立，請參閱警示屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5d36a-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="5d36a-120">-AlertId</span></span>
<span data-ttu-id="5d36a-121">取得或設定提醒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="5d36a-122">-AlertProperty</span></span>
<span data-ttu-id="5d36a-123">警示的屬性。</span><span class="sxs-lookup"><span data-stu-id="5d36a-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="5d36a-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="5d36a-125">關閉通知的使用者別名。</span><span class="sxs-lookup"><span data-stu-id="5d36a-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="5d36a-126">-ClosedTimestamp</span></span>
<span data-ttu-id="5d36a-127">關閉通知時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="5d36a-128">-CreatedTimestamp</span></span>
<span data-ttu-id="5d36a-129">已建立預警的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d36a-130">-DefaultProfile</span></span>
<span data-ttu-id="5d36a-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-132">-描述</span><span class="sxs-lookup"><span data-stu-id="5d36a-132">-Description</span></span>
<span data-ttu-id="5d36a-133">提醒的描述。</span><span class="sxs-lookup"><span data-stu-id="5d36a-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="5d36a-134">-FaultId</span></span>
<span data-ttu-id="5d36a-135">取得或設定提醒的錯誤 ID。</span><span class="sxs-lookup"><span data-stu-id="5d36a-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="5d36a-136">-FaultTypeId</span></span>
<span data-ttu-id="5d36a-137">取得或設定報警的錯誤類型 ID。</span><span class="sxs-lookup"><span data-stu-id="5d36a-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="5d36a-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="5d36a-139">指出是否可修正報警。</span><span class="sxs-lookup"><span data-stu-id="5d36a-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="5d36a-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="5d36a-141">受影響的專案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="5d36a-142">-ImpactedResourceId</span></span>
<span data-ttu-id="5d36a-143">取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d36a-144">-InputObject</span></span>
<span data-ttu-id="5d36a-145">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5d36a-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="5d36a-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="5d36a-147">上次更新警報的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-148">-位置</span><span class="sxs-lookup"><span data-stu-id="5d36a-148">-Location</span></span>
<span data-ttu-id="5d36a-149">地區名稱</span><span class="sxs-lookup"><span data-stu-id="5d36a-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="5d36a-150">-Location1</span></span>
<span data-ttu-id="5d36a-151">資源所在的 Azure 地區</span><span class="sxs-lookup"><span data-stu-id="5d36a-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d36a-152">-Name</span></span>
<span data-ttu-id="5d36a-153">提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-154">-修正</span><span class="sxs-lookup"><span data-stu-id="5d36a-154">-Remediation</span></span>
<span data-ttu-id="5d36a-155">取得或設定提醒的管理員友好修正指示。</span><span class="sxs-lookup"><span data-stu-id="5d36a-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d36a-156">-ResourceGroupName</span></span>
<span data-ttu-id="5d36a-157">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="5d36a-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="5d36a-159">取得或設定報警所屬之服務的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="5d36a-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="5d36a-161">取得或設定與警示相關聯之資源的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="5d36a-162">如果通知沒有與資源相關聯，則資源註冊 ID 為 null。</span><span class="sxs-lookup"><span data-stu-id="5d36a-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-163">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="5d36a-163">-Severity</span></span>
<span data-ttu-id="5d36a-164">警示的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="5d36a-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-165">-State</span><span class="sxs-lookup"><span data-stu-id="5d36a-165">-State</span></span>
<span data-ttu-id="5d36a-166">警示的狀態。</span><span class="sxs-lookup"><span data-stu-id="5d36a-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d36a-167">-SubscriptionId</span></span>
<span data-ttu-id="5d36a-168">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5d36a-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d36a-169">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5d36a-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d36a-170">-Tag</span></span>
<span data-ttu-id="5d36a-171">資源標記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-172">-標題</span><span class="sxs-lookup"><span data-stu-id="5d36a-172">-Title</span></span>
<span data-ttu-id="5d36a-173">取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d36a-174">-使用者</span><span class="sxs-lookup"><span data-stu-id="5d36a-174">-User</span></span>
<span data-ttu-id="5d36a-175">用來執行作業的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="5d36a-176">-確認</span><span class="sxs-lookup"><span data-stu-id="5d36a-176">-Confirm</span></span>
<span data-ttu-id="5d36a-177">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d36a-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d36a-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d36a-178">-WhatIf</span></span>
<span data-ttu-id="5d36a-179">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d36a-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d36a-180">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d36a-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d36a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d36a-181">CommonParameters</span></span>
<span data-ttu-id="5d36a-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d36a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d36a-183">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5d36a-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d36a-184">輸入</span><span class="sxs-lookup"><span data-stu-id="5d36a-184">INPUTS</span></span>

### <span data-ttu-id="5d36a-185">IAlert （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="5d36a-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="5d36a-186">IInfrastructureInsightsAdminIdentity （InfrastructureInsightsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="5d36a-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="5d36a-187">輸出</span><span class="sxs-lookup"><span data-stu-id="5d36a-187">OUTPUTS</span></span>

### <span data-ttu-id="5d36a-188">IAlert （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="5d36a-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="5d36a-189">筆記</span><span class="sxs-lookup"><span data-stu-id="5d36a-189">NOTES</span></span>

<span data-ttu-id="5d36a-190">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5d36a-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d36a-191">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5d36a-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5d36a-192">警示 <IAlert> ：此物件代表警示資源。</span><span class="sxs-lookup"><span data-stu-id="5d36a-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="5d36a-193">`[Location <String>]`：資源所在的 Azure 地區</span><span class="sxs-lookup"><span data-stu-id="5d36a-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="5d36a-194">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="5d36a-195">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="5d36a-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5d36a-196">`[AlertId <String>]`：取得或設定提醒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="5d36a-197">`[AlertProperty <IAlertModelAlertProperties>]`：警示的屬性。</span><span class="sxs-lookup"><span data-stu-id="5d36a-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="5d36a-198">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="5d36a-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5d36a-199">`[ClosedByUserAlias <String>]`：關閉通知的使用者別名。</span><span class="sxs-lookup"><span data-stu-id="5d36a-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="5d36a-200">`[ClosedTimestamp <String>]`：通知關閉時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="5d36a-201">`[CreatedTimestamp <String>]`：預警的建立時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="5d36a-202">`[Description <IDictionary[]>]`：預警的描述。</span><span class="sxs-lookup"><span data-stu-id="5d36a-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="5d36a-203">`[FaultId <String>]`：取得或設定提醒的錯誤 ID。</span><span class="sxs-lookup"><span data-stu-id="5d36a-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="5d36a-204">`[FaultTypeId <String>]`：取得或設定警示的錯誤類型 ID。</span><span class="sxs-lookup"><span data-stu-id="5d36a-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="5d36a-205">`[HasValidRemediationAction <Boolean?>]`：表示是否可修正預警。</span><span class="sxs-lookup"><span data-stu-id="5d36a-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="5d36a-206">`[ImpactedResourceDisplayName <String>]`：受影響的專案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="5d36a-207">`[ImpactedResourceId <String>]`：取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="5d36a-208">`[LastUpdatedTimestamp <String>]`：上次更新警報的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5d36a-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="5d36a-209">`[Remediation <IDictionary[]>]`：取得或設定提醒的管理員友好修正指示。</span><span class="sxs-lookup"><span data-stu-id="5d36a-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="5d36a-210">`[ResourceProviderRegistrationId <String>]`：取得或設定報警所屬之服務的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="5d36a-211">`[ResourceRegistrationId <String>]`：取得或設定與警示相關聯之資源的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="5d36a-212">如果通知沒有與資源相關聯，則資源註冊 ID 為 null。</span><span class="sxs-lookup"><span data-stu-id="5d36a-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="5d36a-213">`[Severity <String>]`：警示的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="5d36a-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="5d36a-214">`[State <String>]`：提醒的狀態。</span><span class="sxs-lookup"><span data-stu-id="5d36a-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="5d36a-215">`[Title <String>]`：取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="5d36a-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5d36a-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d36a-217">`[AlertName <String>]`：警示的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="5d36a-218">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5d36a-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d36a-219">`[Location <String>]`：區域的名稱</span><span class="sxs-lookup"><span data-stu-id="5d36a-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="5d36a-220">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5d36a-221">`[ResourceRegistrationId <String>]`：資源註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d36a-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="5d36a-222">`[ServiceHealth <String>]`：服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="5d36a-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="5d36a-223">`[ServiceRegistrationId <String>]`：服務註冊 ID。</span><span class="sxs-lookup"><span data-stu-id="5d36a-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="5d36a-224">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5d36a-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d36a-225">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5d36a-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d36a-226">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d36a-226">RELATED LINKS</span></span>

