---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: e06cfbb595f9302bf4c7d90846e5a847a24f9322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917258"
---
# <span data-ttu-id="a1451-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="a1451-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="a1451-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1451-102">SYNOPSIS</span></span>
<span data-ttu-id="a1451-103">刪除具有指定訂閱、資源群組及監視器名稱的 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="a1451-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="a1451-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1451-104">SYNTAX</span></span>

### <span data-ttu-id="a1451-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="a1451-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1451-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1451-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1451-107">描述</span><span class="sxs-lookup"><span data-stu-id="a1451-107">DESCRIPTION</span></span>
<span data-ttu-id="a1451-108">刪除具有指定訂閱、資源群組及監視器名稱的 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="a1451-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="a1451-109">例子</span><span class="sxs-lookup"><span data-stu-id="a1451-109">EXAMPLES</span></span>

### <span data-ttu-id="a1451-110">範例 1：根據名稱移除 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="a1451-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="a1451-111">此命令會按名稱移除 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="a1451-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="a1451-112">範例 2：根據物件移除 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="a1451-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="a1451-113">此命令會按物件移除 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="a1451-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="a1451-114">參數</span><span class="sxs-lookup"><span data-stu-id="a1451-114">PARAMETERS</span></span>

### <span data-ttu-id="a1451-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1451-115">-AsJob</span></span>
<span data-ttu-id="a1451-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="a1451-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a1451-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1451-117">-DefaultProfile</span></span>
<span data-ttu-id="a1451-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1451-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1451-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1451-119">-InputObject</span></span>
<span data-ttu-id="a1451-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1451-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1451-121">-Name</span></span>
<span data-ttu-id="a1451-122">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1451-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a1451-123">-NoWait</span></span>
<span data-ttu-id="a1451-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="a1451-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a1451-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1451-125">-PassThru</span></span>
<span data-ttu-id="a1451-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="a1451-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a1451-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1451-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1451-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1451-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1451-129">-SubscriptionId</span></span>
<span data-ttu-id="a1451-130">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1451-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a1451-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a1451-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a1451-132">-Confirm</span></span>
<span data-ttu-id="a1451-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a1451-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1451-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1451-134">-WhatIf</span></span>
<span data-ttu-id="a1451-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1451-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1451-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1451-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1451-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1451-137">CommonParameters</span></span>
<span data-ttu-id="a1451-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1451-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1451-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1451-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1451-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a1451-140">INPUTS</span></span>

### <span data-ttu-id="a1451-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="a1451-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="a1451-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a1451-142">OUTPUTS</span></span>

### <span data-ttu-id="a1451-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1451-143">System.Boolean</span></span>

## <span data-ttu-id="a1451-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a1451-144">NOTES</span></span>

<span data-ttu-id="a1451-145">別名</span><span class="sxs-lookup"><span data-stu-id="a1451-145">ALIASES</span></span>

<span data-ttu-id="a1451-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a1451-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1451-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1451-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1451-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a1451-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1451-149">INPUTOBJECT： <IHanaOnAzureIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a1451-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1451-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a1451-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1451-151">`[Location <String>]`：已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="a1451-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="a1451-152">`[OperationKind <AccessPolicyUpdateKind?>]`：作業名稱</span><span class="sxs-lookup"><span data-stu-id="a1451-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="a1451-153">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1451-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="a1451-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1451-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a1451-155">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1451-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="a1451-156">`[SapMonitorName <String>]`：SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1451-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="a1451-157">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="a1451-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="a1451-158">受管理身分驗證擴充的父資源。</span><span class="sxs-lookup"><span data-stu-id="a1451-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="a1451-159">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1451-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a1451-160">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a1451-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a1451-161">`[VaultName <String>]`：儲存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="a1451-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="a1451-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1451-162">RELATED LINKS</span></span>

