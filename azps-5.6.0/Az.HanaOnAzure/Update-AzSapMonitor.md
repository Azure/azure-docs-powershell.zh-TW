---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 223884fb5974c94b31d8d3ddf2017e1c6e3740b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917253"
---
# <span data-ttu-id="2cc32-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="2cc32-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="2cc32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2cc32-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc32-103">針對指定的訂閱、資源群組和監視器名稱修補 SAP 監視器的標記欄位。</span><span class="sxs-lookup"><span data-stu-id="2cc32-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="2cc32-104">語法</span><span class="sxs-lookup"><span data-stu-id="2cc32-104">SYNTAX</span></span>

### <span data-ttu-id="2cc32-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="2cc32-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2cc32-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2cc32-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2cc32-107">描述</span><span class="sxs-lookup"><span data-stu-id="2cc32-107">DESCRIPTION</span></span>
<span data-ttu-id="2cc32-108">針對指定的訂閱、資源群組和監視器名稱修補 SAP 監視器的標記欄位。</span><span class="sxs-lookup"><span data-stu-id="2cc32-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="2cc32-109">例子</span><span class="sxs-lookup"><span data-stu-id="2cc32-109">EXAMPLES</span></span>

### <span data-ttu-id="2cc32-110">範例 1：根據名稱更新 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="2cc32-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="2cc32-111">這個命令會以名稱更新 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="2cc32-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="2cc32-112">範例 2：根據物件更新 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="2cc32-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="2cc32-113">這個命令會按物件更新 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="2cc32-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="2cc32-114">參數</span><span class="sxs-lookup"><span data-stu-id="2cc32-114">PARAMETERS</span></span>

### <span data-ttu-id="2cc32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc32-115">-DefaultProfile</span></span>
<span data-ttu-id="2cc32-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cc32-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cc32-117">-InputObject</span></span>
<span data-ttu-id="2cc32-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2cc32-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc32-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cc32-119">-Name</span></span>
<span data-ttu-id="2cc32-120">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc32-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc32-121">-ResourceGroupName</span></span>
<span data-ttu-id="2cc32-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-122">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc32-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2cc32-123">-SubscriptionId</span></span>
<span data-ttu-id="2cc32-124">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2cc32-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2cc32-125">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2cc32-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc32-126">-標記</span><span class="sxs-lookup"><span data-stu-id="2cc32-126">-Tag</span></span>
<span data-ttu-id="2cc32-127">資源的標記欄位。</span><span class="sxs-lookup"><span data-stu-id="2cc32-127">Tags field of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc32-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2cc32-128">-Confirm</span></span>
<span data-ttu-id="2cc32-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2cc32-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc32-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc32-130">-WhatIf</span></span>
<span data-ttu-id="2cc32-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2cc32-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cc32-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cc32-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc32-133">CommonParameters</span></span>
<span data-ttu-id="2cc32-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2cc32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc32-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cc32-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc32-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2cc32-136">INPUTS</span></span>

### <span data-ttu-id="2cc32-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="2cc32-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="2cc32-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2cc32-138">OUTPUTS</span></span>

### <span data-ttu-id="2cc32-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="2cc32-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="2cc32-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2cc32-140">NOTES</span></span>

<span data-ttu-id="2cc32-141">別名</span><span class="sxs-lookup"><span data-stu-id="2cc32-141">ALIASES</span></span>

<span data-ttu-id="2cc32-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2cc32-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2cc32-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2cc32-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2cc32-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2cc32-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2cc32-145">INPUTOBJECT： <IHanaOnAzureIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2cc32-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2cc32-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2cc32-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2cc32-147">`[Location <String>]`：已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="2cc32-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="2cc32-148">`[OperationKind <AccessPolicyUpdateKind?>]`：作業名稱</span><span class="sxs-lookup"><span data-stu-id="2cc32-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="2cc32-149">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="2cc32-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2cc32-151">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="2cc32-152">`[SapMonitorName <String>]`：SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc32-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="2cc32-153">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="2cc32-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="2cc32-154">受管理身分驗證擴充的父資源。</span><span class="sxs-lookup"><span data-stu-id="2cc32-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="2cc32-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2cc32-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2cc32-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2cc32-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2cc32-157">`[VaultName <String>]`：儲存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="2cc32-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="2cc32-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cc32-158">RELATED LINKS</span></span>

