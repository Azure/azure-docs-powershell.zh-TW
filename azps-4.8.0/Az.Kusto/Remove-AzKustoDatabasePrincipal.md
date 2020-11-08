---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135942"
---
# <span data-ttu-id="d5db4-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="d5db4-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="d5db4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5db4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5db4-103">移除資料庫主體許可權。</span><span class="sxs-lookup"><span data-stu-id="d5db4-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="d5db4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5db4-104">SYNTAX</span></span>

### <span data-ttu-id="d5db4-105">RemoveExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="d5db4-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d5db4-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d5db4-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5db4-107">說明</span><span class="sxs-lookup"><span data-stu-id="d5db4-107">DESCRIPTION</span></span>
<span data-ttu-id="d5db4-108">移除資料庫主體許可權。</span><span class="sxs-lookup"><span data-stu-id="d5db4-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="d5db4-109">示例</span><span class="sxs-lookup"><span data-stu-id="d5db4-109">EXAMPLES</span></span>

### <span data-ttu-id="d5db4-110">範例1：移除資料庫主體許可權</span><span class="sxs-lookup"><span data-stu-id="d5db4-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="d5db4-111">上述命令會移除資料庫主體許可權</span><span class="sxs-lookup"><span data-stu-id="d5db4-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="d5db4-112">參數</span><span class="sxs-lookup"><span data-stu-id="d5db4-112">PARAMETERS</span></span>

### <span data-ttu-id="d5db4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d5db4-113">-ClusterName</span></span>
<span data-ttu-id="d5db4-114">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d5db4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5db4-115">-DatabaseName</span></span>
<span data-ttu-id="d5db4-116">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d5db4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5db4-117">-DefaultProfile</span></span>
<span data-ttu-id="d5db4-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5db4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5db4-119">-InputObject</span></span>
<span data-ttu-id="d5db4-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d5db4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5db4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5db4-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5db4-122">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d5db4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5db4-123">-SubscriptionId</span></span>
<span data-ttu-id="d5db4-124">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d5db4-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5db4-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d5db4-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5db4-126">-值</span><span class="sxs-lookup"><span data-stu-id="d5db4-126">-Value</span></span>
<span data-ttu-id="d5db4-127">Kusto 資料庫主體的清單。</span><span class="sxs-lookup"><span data-stu-id="d5db4-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="d5db4-128">若要建立，請參閱值屬性的記事區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d5db4-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5db4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d5db4-129">-Confirm</span></span>
<span data-ttu-id="d5db4-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5db4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5db4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5db4-131">-WhatIf</span></span>
<span data-ttu-id="d5db4-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5db4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5db4-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5db4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5db4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5db4-134">CommonParameters</span></span>
<span data-ttu-id="d5db4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5db4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5db4-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5db4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5db4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d5db4-137">INPUTS</span></span>

### <span data-ttu-id="d5db4-138">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="d5db4-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d5db4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d5db4-139">OUTPUTS</span></span>

### <span data-ttu-id="d5db4-140">IDatabasePrincipal （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="d5db4-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="d5db4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d5db4-141">NOTES</span></span>

<span data-ttu-id="d5db4-142">別名</span><span class="sxs-lookup"><span data-stu-id="d5db4-142">ALIASES</span></span>

<span data-ttu-id="d5db4-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d5db4-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5db4-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d5db4-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5db4-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d5db4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5db4-146">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d5db4-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5db4-147">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d5db4-148">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d5db4-149">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d5db4-150">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d5db4-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d5db4-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5db4-152">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="d5db4-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d5db4-153">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d5db4-154">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d5db4-155">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d5db4-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d5db4-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d5db4-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d5db4-157">VALUE <IDatabasePrincipal [] >： Kusto 資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="d5db4-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="d5db4-158">`Name <String>`：資料庫主要名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="d5db4-159">`Role <DatabasePrincipalRole>`：資料庫主體角色。</span><span class="sxs-lookup"><span data-stu-id="d5db4-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="d5db4-160">`Type <DatabasePrincipalType>`：資料庫主體類型。</span><span class="sxs-lookup"><span data-stu-id="d5db4-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="d5db4-161">`[AppId <String>]`：應用程式識別碼-僅適用于應用程式主體類型。</span><span class="sxs-lookup"><span data-stu-id="d5db4-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="d5db4-162">`[Email <String>]`：資料庫主要電子郵件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d5db4-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="d5db4-163">`[Fqn <String>]`：資料庫主體的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="d5db4-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="d5db4-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5db4-164">RELATED LINKS</span></span>

