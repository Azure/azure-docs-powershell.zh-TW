---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 630393d0c535a5f44f8a5e7dcf49cc491552f185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917254"
---
# <span data-ttu-id="dda31-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="dda31-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="dda31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dda31-102">SYNOPSIS</span></span>
<span data-ttu-id="dda31-103">刪除指定訂閱、資源群組、SapMonitor 名稱和資源名稱的提供者實例。</span><span class="sxs-lookup"><span data-stu-id="dda31-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="dda31-104">語法</span><span class="sxs-lookup"><span data-stu-id="dda31-104">SYNTAX</span></span>

### <span data-ttu-id="dda31-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="dda31-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dda31-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dda31-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dda31-107">描述</span><span class="sxs-lookup"><span data-stu-id="dda31-107">DESCRIPTION</span></span>
<span data-ttu-id="dda31-108">刪除指定訂閱、資源群組、SapMonitor 名稱和資源名稱的提供者實例。</span><span class="sxs-lookup"><span data-stu-id="dda31-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="dda31-109">例子</span><span class="sxs-lookup"><span data-stu-id="dda31-109">EXAMPLES</span></span>

### <span data-ttu-id="dda31-110">範例 1：根據名稱移除 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="dda31-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="dda31-111">此命令會按名稱移除 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="dda31-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="dda31-112">範例 2：根據物件移除 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="dda31-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="dda31-113">此命令會按物件移除 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="dda31-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="dda31-114">參數</span><span class="sxs-lookup"><span data-stu-id="dda31-114">PARAMETERS</span></span>

### <span data-ttu-id="dda31-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dda31-115">-AsJob</span></span>
<span data-ttu-id="dda31-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="dda31-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dda31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda31-117">-DefaultProfile</span></span>
<span data-ttu-id="dda31-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dda31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dda31-119">-InputObject</span></span>
<span data-ttu-id="dda31-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dda31-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dda31-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dda31-121">-Name</span></span>
<span data-ttu-id="dda31-122">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda31-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dda31-123">-NoWait</span></span>
<span data-ttu-id="dda31-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="dda31-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dda31-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dda31-125">-PassThru</span></span>
<span data-ttu-id="dda31-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="dda31-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dda31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda31-127">-ResourceGroupName</span></span>
<span data-ttu-id="dda31-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="dda31-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="dda31-129">-SapMonitorName</span></span>
<span data-ttu-id="dda31-130">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="dda31-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dda31-131">-SubscriptionId</span></span>
<span data-ttu-id="dda31-132">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="dda31-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dda31-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="dda31-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dda31-134">-確認</span><span class="sxs-lookup"><span data-stu-id="dda31-134">-Confirm</span></span>
<span data-ttu-id="dda31-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dda31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda31-136">-WhatIf</span></span>
<span data-ttu-id="dda31-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dda31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda31-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dda31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda31-139">CommonParameters</span></span>
<span data-ttu-id="dda31-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dda31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda31-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dda31-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda31-142">輸入</span><span class="sxs-lookup"><span data-stu-id="dda31-142">INPUTS</span></span>

### <span data-ttu-id="dda31-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="dda31-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="dda31-144">輸出</span><span class="sxs-lookup"><span data-stu-id="dda31-144">OUTPUTS</span></span>

### <span data-ttu-id="dda31-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dda31-145">System.Boolean</span></span>

## <span data-ttu-id="dda31-146">筆記</span><span class="sxs-lookup"><span data-stu-id="dda31-146">NOTES</span></span>

<span data-ttu-id="dda31-147">別名</span><span class="sxs-lookup"><span data-stu-id="dda31-147">ALIASES</span></span>

<span data-ttu-id="dda31-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dda31-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dda31-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dda31-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dda31-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dda31-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dda31-151">INPUTOBJECT： <IHanaOnAzureIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dda31-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dda31-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="dda31-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dda31-153">`[Location <String>]`：已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="dda31-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="dda31-154">`[OperationKind <AccessPolicyUpdateKind?>]`：作業名稱</span><span class="sxs-lookup"><span data-stu-id="dda31-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="dda31-155">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="dda31-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dda31-157">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="dda31-158">`[SapMonitorName <String>]`：SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="dda31-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="dda31-159">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="dda31-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="dda31-160">受管理身分驗證擴充的父資源。</span><span class="sxs-lookup"><span data-stu-id="dda31-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="dda31-161">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="dda31-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dda31-162">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="dda31-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dda31-163">`[VaultName <String>]`：儲存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="dda31-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="dda31-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="dda31-164">RELATED LINKS</span></span>

