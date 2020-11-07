---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968302"
---
# <span data-ttu-id="0b902-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="0b902-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="0b902-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b902-102">SYNOPSIS</span></span>
<span data-ttu-id="0b902-103">修復提醒。</span><span class="sxs-lookup"><span data-stu-id="0b902-103">Repairs an alert.</span></span>

## <span data-ttu-id="0b902-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b902-104">SYNTAX</span></span>

### <span data-ttu-id="0b902-105">修復 (預設) </span><span class="sxs-lookup"><span data-stu-id="0b902-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b902-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0b902-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b902-107">說明</span><span class="sxs-lookup"><span data-stu-id="0b902-107">DESCRIPTION</span></span>
<span data-ttu-id="0b902-108">修復提醒。</span><span class="sxs-lookup"><span data-stu-id="0b902-108">Repairs an alert.</span></span>

## <span data-ttu-id="0b902-109">示例</span><span class="sxs-lookup"><span data-stu-id="0b902-109">EXAMPLES</span></span>

### <span data-ttu-id="0b902-110">範例1：</span><span class="sxs-lookup"><span data-stu-id="0b902-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="0b902-111">透過名稱來修復警示。</span><span class="sxs-lookup"><span data-stu-id="0b902-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="0b902-112">範例2：</span><span class="sxs-lookup"><span data-stu-id="0b902-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="0b902-113">透過 [管道] 修復警示。</span><span class="sxs-lookup"><span data-stu-id="0b902-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="0b902-114">參數</span><span class="sxs-lookup"><span data-stu-id="0b902-114">PARAMETERS</span></span>

### <span data-ttu-id="0b902-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b902-115">-AsJob</span></span>
<span data-ttu-id="0b902-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="0b902-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0b902-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b902-117">-DefaultProfile</span></span>
<span data-ttu-id="0b902-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b902-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b902-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b902-119">-InputObject</span></span>
<span data-ttu-id="0b902-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0b902-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0b902-121">-位置</span><span class="sxs-lookup"><span data-stu-id="0b902-121">-Location</span></span>
<span data-ttu-id="0b902-122">地區名稱</span><span class="sxs-lookup"><span data-stu-id="0b902-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b902-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b902-123">-Name</span></span>
<span data-ttu-id="0b902-124">提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b902-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b902-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0b902-125">-NoWait</span></span>
<span data-ttu-id="0b902-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="0b902-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0b902-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b902-127">-PassThru</span></span>
<span data-ttu-id="0b902-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="0b902-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0b902-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b902-129">-ResourceGroupName</span></span>
<span data-ttu-id="0b902-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b902-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b902-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b902-131">-SubscriptionId</span></span>
<span data-ttu-id="0b902-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0b902-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0b902-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0b902-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b902-134">-確認</span><span class="sxs-lookup"><span data-stu-id="0b902-134">-Confirm</span></span>
<span data-ttu-id="0b902-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b902-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b902-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b902-136">-WhatIf</span></span>
<span data-ttu-id="0b902-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b902-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b902-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b902-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b902-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b902-139">CommonParameters</span></span>
<span data-ttu-id="0b902-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b902-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b902-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b902-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b902-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0b902-142">INPUTS</span></span>

### <span data-ttu-id="0b902-143">IInfrastructureInsightsAdminIdentity （InfrastructureInsightsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="0b902-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="0b902-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0b902-144">OUTPUTS</span></span>

### <span data-ttu-id="0b902-145">System.object</span><span class="sxs-lookup"><span data-stu-id="0b902-145">System.Boolean</span></span>



## <span data-ttu-id="0b902-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0b902-146">NOTES</span></span>

<span data-ttu-id="0b902-147">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0b902-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b902-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0b902-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0b902-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0b902-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b902-150">`[AlertName <String>]`：警示的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b902-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="0b902-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0b902-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b902-152">`[Location <String>]`：區域的名稱</span><span class="sxs-lookup"><span data-stu-id="0b902-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="0b902-153">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b902-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0b902-154">`[ResourceRegistrationId <String>]`：資源註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b902-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="0b902-155">`[ServiceHealth <String>]`：服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="0b902-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="0b902-156">`[ServiceRegistrationId <String>]`：服務註冊 ID。</span><span class="sxs-lookup"><span data-stu-id="0b902-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="0b902-157">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0b902-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0b902-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0b902-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0b902-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b902-159">RELATED LINKS</span></span>

