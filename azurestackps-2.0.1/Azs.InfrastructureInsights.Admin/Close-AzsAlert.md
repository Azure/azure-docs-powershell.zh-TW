---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966745"
---
# <span data-ttu-id="cbf04-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="cbf04-101">Close-AzsAlert</span></span>

## <span data-ttu-id="cbf04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbf04-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf04-103">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="cbf04-103">Closes the given alert.</span></span>

## <span data-ttu-id="cbf04-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbf04-104">SYNTAX</span></span>

### <span data-ttu-id="cbf04-105">CloseExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cbf04-105">CloseExpanded (Default)</span></span>
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

### <span data-ttu-id="cbf04-106">結轉</span><span class="sxs-lookup"><span data-stu-id="cbf04-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cbf04-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cbf04-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cbf04-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cbf04-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cbf04-109">說明</span><span class="sxs-lookup"><span data-stu-id="cbf04-109">DESCRIPTION</span></span>
<span data-ttu-id="cbf04-110">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="cbf04-110">Closes the given alert.</span></span>

## <span data-ttu-id="cbf04-111">示例</span><span class="sxs-lookup"><span data-stu-id="cbf04-111">EXAMPLES</span></span>

### <span data-ttu-id="cbf04-112">範例1：</span><span class="sxs-lookup"><span data-stu-id="cbf04-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="cbf04-113">依名稱關閉警示。</span><span class="sxs-lookup"><span data-stu-id="cbf04-113">Close an alert by Name.</span></span>

### <span data-ttu-id="cbf04-114">範例2：</span><span class="sxs-lookup"><span data-stu-id="cbf04-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="cbf04-115">透過 [管道] 關閉警示。</span><span class="sxs-lookup"><span data-stu-id="cbf04-115">Close an alert through piping.</span></span>

## <span data-ttu-id="cbf04-116">參數</span><span class="sxs-lookup"><span data-stu-id="cbf04-116">PARAMETERS</span></span>

### <span data-ttu-id="cbf04-117">-提醒</span><span class="sxs-lookup"><span data-stu-id="cbf04-117">-Alert</span></span>
<span data-ttu-id="cbf04-118">這個物件代表警示資源。</span><span class="sxs-lookup"><span data-stu-id="cbf04-118">This object represents an alert resource.</span></span>
<span data-ttu-id="cbf04-119">若要建立，請參閱警示屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="cbf04-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbf04-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="cbf04-120">-AlertId</span></span>
<span data-ttu-id="cbf04-121">取得或設定提醒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-121">Gets or sets the ID of the alert.</span></span>

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

### <span data-ttu-id="cbf04-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="cbf04-122">-AlertProperty</span></span>
<span data-ttu-id="cbf04-123">警示的屬性。</span><span class="sxs-lookup"><span data-stu-id="cbf04-123">Properties of the alert.</span></span>

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

### <span data-ttu-id="cbf04-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="cbf04-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="cbf04-125">關閉通知的使用者別名。</span><span class="sxs-lookup"><span data-stu-id="cbf04-125">User alias who closed the alert.</span></span>

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

### <span data-ttu-id="cbf04-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="cbf04-126">-ClosedTimestamp</span></span>
<span data-ttu-id="cbf04-127">關閉通知時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-127">Timestamp when the alert was closed.</span></span>

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

### <span data-ttu-id="cbf04-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="cbf04-128">-CreatedTimestamp</span></span>
<span data-ttu-id="cbf04-129">已建立預警的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-129">Timestamp when the alert was created.</span></span>

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

### <span data-ttu-id="cbf04-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf04-130">-DefaultProfile</span></span>
<span data-ttu-id="cbf04-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf04-132">-描述</span><span class="sxs-lookup"><span data-stu-id="cbf04-132">-Description</span></span>
<span data-ttu-id="cbf04-133">提醒的描述。</span><span class="sxs-lookup"><span data-stu-id="cbf04-133">Description of the alert.</span></span>

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

### <span data-ttu-id="cbf04-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="cbf04-134">-FaultId</span></span>
<span data-ttu-id="cbf04-135">取得或設定提醒的錯誤 ID。</span><span class="sxs-lookup"><span data-stu-id="cbf04-135">Gets or sets the fault ID of the alert.</span></span>

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

### <span data-ttu-id="cbf04-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="cbf04-136">-FaultTypeId</span></span>
<span data-ttu-id="cbf04-137">取得或設定報警的錯誤類型 ID。</span><span class="sxs-lookup"><span data-stu-id="cbf04-137">Gets or sets the fault type ID of the alert.</span></span>

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

### <span data-ttu-id="cbf04-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="cbf04-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="cbf04-139">指出是否可修正報警。</span><span class="sxs-lookup"><span data-stu-id="cbf04-139">Indicates if the alert can be remediated.</span></span>

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

### <span data-ttu-id="cbf04-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="cbf04-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="cbf04-141">受影響的專案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-141">Display name for the impacted item.</span></span>

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

### <span data-ttu-id="cbf04-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf04-142">-ImpactedResourceId</span></span>
<span data-ttu-id="cbf04-143">取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-143">Gets or sets the Resource ID for the impacted item.</span></span>

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

### <span data-ttu-id="cbf04-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbf04-144">-InputObject</span></span>
<span data-ttu-id="cbf04-145">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbf04-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbf04-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="cbf04-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="cbf04-147">上次更新警報的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-147">Timestamp when the alert was last updated.</span></span>

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

### <span data-ttu-id="cbf04-148">-位置</span><span class="sxs-lookup"><span data-stu-id="cbf04-148">-Location</span></span>
<span data-ttu-id="cbf04-149">地區名稱</span><span class="sxs-lookup"><span data-stu-id="cbf04-149">Name of the region</span></span>

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

### <span data-ttu-id="cbf04-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="cbf04-150">-Location1</span></span>
<span data-ttu-id="cbf04-151">資源所在的 Azure 地區</span><span class="sxs-lookup"><span data-stu-id="cbf04-151">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="cbf04-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbf04-152">-Name</span></span>
<span data-ttu-id="cbf04-153">提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-153">Name of the alert.</span></span>

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

### <span data-ttu-id="cbf04-154">-修正</span><span class="sxs-lookup"><span data-stu-id="cbf04-154">-Remediation</span></span>
<span data-ttu-id="cbf04-155">取得或設定提醒的管理員友好修正指示。</span><span class="sxs-lookup"><span data-stu-id="cbf04-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

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

### <span data-ttu-id="cbf04-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf04-156">-ResourceGroupName</span></span>
<span data-ttu-id="cbf04-157">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-157">The name of the resource group.</span></span>

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

### <span data-ttu-id="cbf04-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="cbf04-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="cbf04-159">取得或設定報警所屬之服務的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

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

### <span data-ttu-id="cbf04-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="cbf04-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="cbf04-161">取得或設定與警示相關聯之資源的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="cbf04-162">如果通知沒有與資源相關聯，則資源註冊 ID 為 null。</span><span class="sxs-lookup"><span data-stu-id="cbf04-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

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

### <span data-ttu-id="cbf04-163">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="cbf04-163">-Severity</span></span>
<span data-ttu-id="cbf04-164">警示的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="cbf04-164">Severity of the alert.</span></span>

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

### <span data-ttu-id="cbf04-165">-State</span><span class="sxs-lookup"><span data-stu-id="cbf04-165">-State</span></span>
<span data-ttu-id="cbf04-166">警示的狀態。</span><span class="sxs-lookup"><span data-stu-id="cbf04-166">State of the alert.</span></span>

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

### <span data-ttu-id="cbf04-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbf04-167">-SubscriptionId</span></span>
<span data-ttu-id="cbf04-168">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cbf04-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cbf04-169">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cbf04-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cbf04-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="cbf04-170">-Tag</span></span>
<span data-ttu-id="cbf04-171">資源標記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-171">Resource tags.</span></span>

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

### <span data-ttu-id="cbf04-172">-標題</span><span class="sxs-lookup"><span data-stu-id="cbf04-172">-Title</span></span>
<span data-ttu-id="cbf04-173">取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-173">Gets or sets the Resource ID for the impacted item.</span></span>

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

### <span data-ttu-id="cbf04-174">-使用者</span><span class="sxs-lookup"><span data-stu-id="cbf04-174">-User</span></span>
<span data-ttu-id="cbf04-175">用來執行作業的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="cbf04-176">-確認</span><span class="sxs-lookup"><span data-stu-id="cbf04-176">-Confirm</span></span>
<span data-ttu-id="cbf04-177">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbf04-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbf04-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf04-178">-WhatIf</span></span>
<span data-ttu-id="cbf04-179">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbf04-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf04-180">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbf04-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbf04-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf04-181">CommonParameters</span></span>
<span data-ttu-id="cbf04-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbf04-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf04-183">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cbf04-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf04-184">輸入</span><span class="sxs-lookup"><span data-stu-id="cbf04-184">INPUTS</span></span>

### <span data-ttu-id="cbf04-185">IAlert （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="cbf04-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="cbf04-186">IInfrastructureInsightsAdminIdentity （InfrastructureInsightsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="cbf04-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="cbf04-187">輸出</span><span class="sxs-lookup"><span data-stu-id="cbf04-187">OUTPUTS</span></span>

### <span data-ttu-id="cbf04-188">IAlert （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="cbf04-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="cbf04-189">筆記</span><span class="sxs-lookup"><span data-stu-id="cbf04-189">NOTES</span></span>

<span data-ttu-id="cbf04-190">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cbf04-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbf04-191">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cbf04-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cbf04-192">警示 <IAlert> ：此物件代表警示資源。</span><span class="sxs-lookup"><span data-stu-id="cbf04-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="cbf04-193">`[Location <String>]`：資源所在的 Azure 地區</span><span class="sxs-lookup"><span data-stu-id="cbf04-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="cbf04-194">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="cbf04-195">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="cbf04-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cbf04-196">`[AlertId <String>]`：取得或設定提醒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="cbf04-197">`[AlertProperty <IAlertModelAlertProperties>]`：警示的屬性。</span><span class="sxs-lookup"><span data-stu-id="cbf04-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="cbf04-198">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="cbf04-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cbf04-199">`[ClosedByUserAlias <String>]`：關閉通知的使用者別名。</span><span class="sxs-lookup"><span data-stu-id="cbf04-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="cbf04-200">`[ClosedTimestamp <String>]`：通知關閉時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="cbf04-201">`[CreatedTimestamp <String>]`：預警的建立時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="cbf04-202">`[Description <IDictionary[]>]`：預警的描述。</span><span class="sxs-lookup"><span data-stu-id="cbf04-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="cbf04-203">`[FaultId <String>]`：取得或設定提醒的錯誤 ID。</span><span class="sxs-lookup"><span data-stu-id="cbf04-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="cbf04-204">`[FaultTypeId <String>]`：取得或設定警示的錯誤類型 ID。</span><span class="sxs-lookup"><span data-stu-id="cbf04-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="cbf04-205">`[HasValidRemediationAction <Boolean?>]`：表示是否可修正預警。</span><span class="sxs-lookup"><span data-stu-id="cbf04-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="cbf04-206">`[ImpactedResourceDisplayName <String>]`：受影響的專案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="cbf04-207">`[ImpactedResourceId <String>]`：取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="cbf04-208">`[LastUpdatedTimestamp <String>]`：上次更新警報的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cbf04-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="cbf04-209">`[Remediation <IDictionary[]>]`：取得或設定提醒的管理員友好修正指示。</span><span class="sxs-lookup"><span data-stu-id="cbf04-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="cbf04-210">`[ResourceProviderRegistrationId <String>]`：取得或設定報警所屬之服務的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="cbf04-211">`[ResourceRegistrationId <String>]`：取得或設定與警示相關聯之資源的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="cbf04-212">如果通知沒有與資源相關聯，則資源註冊 ID 為 null。</span><span class="sxs-lookup"><span data-stu-id="cbf04-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="cbf04-213">`[Severity <String>]`：警示的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="cbf04-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="cbf04-214">`[State <String>]`：提醒的狀態。</span><span class="sxs-lookup"><span data-stu-id="cbf04-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="cbf04-215">`[Title <String>]`：取得或設定受影響專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="cbf04-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cbf04-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbf04-217">`[AlertName <String>]`：警示的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="cbf04-218">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cbf04-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbf04-219">`[Location <String>]`：區域的名稱</span><span class="sxs-lookup"><span data-stu-id="cbf04-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="cbf04-220">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cbf04-221">`[ResourceRegistrationId <String>]`：資源註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf04-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="cbf04-222">`[ServiceHealth <String>]`：服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf04-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="cbf04-223">`[ServiceRegistrationId <String>]`：服務註冊 ID。</span><span class="sxs-lookup"><span data-stu-id="cbf04-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="cbf04-224">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cbf04-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cbf04-225">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cbf04-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cbf04-226">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbf04-226">RELATED LINKS</span></span>
