---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438228"
---
# <span data-ttu-id="8198b-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="8198b-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="8198b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8198b-102">SYNOPSIS</span></span>
<span data-ttu-id="8198b-103">針對指定的訂閱、資源群組及監視器名稱，修補 SAP 監視器的 [標籤] 欄位。</span><span class="sxs-lookup"><span data-stu-id="8198b-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="8198b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8198b-104">SYNTAX</span></span>

### <span data-ttu-id="8198b-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8198b-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8198b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8198b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8198b-107">說明</span><span class="sxs-lookup"><span data-stu-id="8198b-107">DESCRIPTION</span></span>
<span data-ttu-id="8198b-108">針對指定的訂閱、資源群組及監視器名稱，修補 SAP 監視器的 [標籤] 欄位。</span><span class="sxs-lookup"><span data-stu-id="8198b-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="8198b-109">示例</span><span class="sxs-lookup"><span data-stu-id="8198b-109">EXAMPLES</span></span>

### <span data-ttu-id="8198b-110">範例1：依名稱更新 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="8198b-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="8198b-111">這個命令會依名稱更新 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="8198b-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="8198b-112">範例2：依物件更新 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="8198b-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="8198b-113">這個命令會依物件更新 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="8198b-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="8198b-114">參數</span><span class="sxs-lookup"><span data-stu-id="8198b-114">PARAMETERS</span></span>

### <span data-ttu-id="8198b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8198b-115">-DefaultProfile</span></span>
<span data-ttu-id="8198b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8198b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8198b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8198b-117">-InputObject</span></span>
<span data-ttu-id="8198b-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8198b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8198b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8198b-119">-Name</span></span>
<span data-ttu-id="8198b-120">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8198b-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="8198b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8198b-121">-ResourceGroupName</span></span>
<span data-ttu-id="8198b-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8198b-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="8198b-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8198b-123">-SubscriptionId</span></span>
<span data-ttu-id="8198b-124">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="8198b-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8198b-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8198b-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8198b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8198b-126">-Tag</span></span>
<span data-ttu-id="8198b-127">資源的 [標記] 欄位。</span><span class="sxs-lookup"><span data-stu-id="8198b-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="8198b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8198b-128">-Confirm</span></span>
<span data-ttu-id="8198b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8198b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8198b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8198b-130">-WhatIf</span></span>
<span data-ttu-id="8198b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8198b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8198b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8198b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8198b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8198b-133">CommonParameters</span></span>
<span data-ttu-id="8198b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8198b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8198b-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8198b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8198b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8198b-136">INPUTS</span></span>

### <span data-ttu-id="8198b-137">IHanaOnAzureIdentity （HanaOnAzure）的</span><span class="sxs-lookup"><span data-stu-id="8198b-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="8198b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8198b-138">OUTPUTS</span></span>

### <span data-ttu-id="8198b-139">ISapMonitor （HanaOnAzure）。 Api20200207Preview。</span><span class="sxs-lookup"><span data-stu-id="8198b-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="8198b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8198b-140">NOTES</span></span>

<span data-ttu-id="8198b-141">別名</span><span class="sxs-lookup"><span data-stu-id="8198b-141">ALIASES</span></span>

<span data-ttu-id="8198b-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8198b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8198b-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8198b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8198b-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8198b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8198b-145">INPUTOBJECT <IHanaOnAzureIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8198b-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8198b-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8198b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8198b-147">`[Location <String>]`：已刪除的保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="8198b-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="8198b-148">`[OperationKind <AccessPolicyUpdateKind?>]`：操作的名稱</span><span class="sxs-lookup"><span data-stu-id="8198b-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="8198b-149">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="8198b-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="8198b-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8198b-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8198b-151">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8198b-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="8198b-152">`[SapMonitorName <String>]`： SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8198b-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="8198b-153">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="8198b-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="8198b-154">受管理的身分識別的父資源。</span><span class="sxs-lookup"><span data-stu-id="8198b-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="8198b-155">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8198b-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8198b-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8198b-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8198b-157">`[VaultName <String>]`：保存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="8198b-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="8198b-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="8198b-158">RELATED LINKS</span></span>

