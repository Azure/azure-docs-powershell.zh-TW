---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 931b808838503ab6bf481225e6f5994326ef8319
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913850"
---
# <span data-ttu-id="6128a-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="6128a-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="6128a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6128a-102">SYNOPSIS</span></span>
<span data-ttu-id="6128a-103">移除資料庫主體許可權。</span><span class="sxs-lookup"><span data-stu-id="6128a-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="6128a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6128a-104">SYNTAX</span></span>

### <span data-ttu-id="6128a-105">RemoveExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6128a-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6128a-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6128a-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6128a-107">描述</span><span class="sxs-lookup"><span data-stu-id="6128a-107">DESCRIPTION</span></span>
<span data-ttu-id="6128a-108">移除資料庫主體許可權。</span><span class="sxs-lookup"><span data-stu-id="6128a-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="6128a-109">例子</span><span class="sxs-lookup"><span data-stu-id="6128a-109">EXAMPLES</span></span>

### <span data-ttu-id="6128a-110">範例 1：移除資料庫主體許可權</span><span class="sxs-lookup"><span data-stu-id="6128a-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="6128a-111">上述命令會移除資料庫主體許可權</span><span class="sxs-lookup"><span data-stu-id="6128a-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="6128a-112">參數</span><span class="sxs-lookup"><span data-stu-id="6128a-112">PARAMETERS</span></span>

### <span data-ttu-id="6128a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6128a-113">-ClusterName</span></span>
<span data-ttu-id="6128a-114">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="6128a-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6128a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6128a-115">-DatabaseName</span></span>
<span data-ttu-id="6128a-116">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6128a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6128a-117">-DefaultProfile</span></span>
<span data-ttu-id="6128a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6128a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6128a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6128a-119">-InputObject</span></span>
<span data-ttu-id="6128a-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6128a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6128a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6128a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6128a-122">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6128a-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6128a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6128a-123">-SubscriptionId</span></span>
<span data-ttu-id="6128a-124">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6128a-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6128a-125">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6128a-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6128a-126">-值</span><span class="sxs-lookup"><span data-stu-id="6128a-126">-Value</span></span>
<span data-ttu-id="6128a-127">Kusto 資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="6128a-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="6128a-128">若要建構，請參閱 VALUE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6128a-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6128a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="6128a-129">-Confirm</span></span>
<span data-ttu-id="6128a-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6128a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6128a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6128a-131">-WhatIf</span></span>
<span data-ttu-id="6128a-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6128a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6128a-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6128a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6128a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6128a-134">CommonParameters</span></span>
<span data-ttu-id="6128a-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6128a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6128a-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6128a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6128a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="6128a-137">INPUTS</span></span>

### <span data-ttu-id="6128a-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="6128a-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6128a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6128a-139">OUTPUTS</span></span>

### <span data-ttu-id="6128a-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="6128a-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="6128a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6128a-141">NOTES</span></span>

<span data-ttu-id="6128a-142">別名</span><span class="sxs-lookup"><span data-stu-id="6128a-142">ALIASES</span></span>

<span data-ttu-id="6128a-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6128a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6128a-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6128a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6128a-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6128a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6128a-146">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6128a-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6128a-147">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6128a-148">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="6128a-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6128a-149">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6128a-150">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6128a-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6128a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6128a-152">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="6128a-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6128a-153">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6128a-154">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6128a-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6128a-155">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6128a-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6128a-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6128a-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="6128a-157">VALUE <IDatabasePrincipal[]>：Kusto 資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="6128a-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="6128a-158">`Name <String>`：資料庫主體名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="6128a-159">`Role <DatabasePrincipalRole>`：資料庫主體角色。</span><span class="sxs-lookup"><span data-stu-id="6128a-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="6128a-160">`Type <DatabasePrincipalType>`：資料庫主體類型。</span><span class="sxs-lookup"><span data-stu-id="6128a-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="6128a-161">`[AppId <String>]`：應用程式識別碼 - 僅與應用程式主體類型相關。</span><span class="sxs-lookup"><span data-stu-id="6128a-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="6128a-162">`[Email <String>]`：如果有資料庫主體電子郵件。</span><span class="sxs-lookup"><span data-stu-id="6128a-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="6128a-163">`[Fqn <String>]`：資料庫主體完整名稱。</span><span class="sxs-lookup"><span data-stu-id="6128a-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="6128a-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="6128a-164">RELATED LINKS</span></span>

