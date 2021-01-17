---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 7c88924f077160fa65031ff06afe453db8f1ee8d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449209"
---
# <span data-ttu-id="b1acc-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="b1acc-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="b1acc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1acc-102">SYNOPSIS</span></span>
<span data-ttu-id="b1acc-103">新增資料庫主體許可權。</span><span class="sxs-lookup"><span data-stu-id="b1acc-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="b1acc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1acc-104">SYNTAX</span></span>

### <span data-ttu-id="b1acc-105">AddExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b1acc-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b1acc-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b1acc-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1acc-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1acc-107">DESCRIPTION</span></span>
<span data-ttu-id="b1acc-108">新增資料庫主體許可權。</span><span class="sxs-lookup"><span data-stu-id="b1acc-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="b1acc-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1acc-109">EXAMPLES</span></span>

### <span data-ttu-id="b1acc-110">範例1：新增資料庫主體許可權</span><span class="sxs-lookup"><span data-stu-id="b1acc-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="b1acc-111">上述命令會新增資料庫主體許可權</span><span class="sxs-lookup"><span data-stu-id="b1acc-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="b1acc-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1acc-112">PARAMETERS</span></span>

### <span data-ttu-id="b1acc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b1acc-113">-ClusterName</span></span>
<span data-ttu-id="b1acc-114">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1acc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1acc-115">-DatabaseName</span></span>
<span data-ttu-id="b1acc-116">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1acc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1acc-117">-DefaultProfile</span></span>
<span data-ttu-id="b1acc-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1acc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1acc-119">-InputObject</span></span>
<span data-ttu-id="b1acc-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1acc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1acc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1acc-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1acc-122">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1acc-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1acc-123">-SubscriptionId</span></span>
<span data-ttu-id="b1acc-124">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b1acc-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1acc-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b1acc-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1acc-126">-值</span><span class="sxs-lookup"><span data-stu-id="b1acc-126">-Value</span></span>
<span data-ttu-id="b1acc-127">Kusto 資料庫主體的清單。</span><span class="sxs-lookup"><span data-stu-id="b1acc-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="b1acc-128">若要建立，請參閱值屬性的記事區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b1acc-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1acc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b1acc-129">-Confirm</span></span>
<span data-ttu-id="b1acc-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1acc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1acc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1acc-131">-WhatIf</span></span>
<span data-ttu-id="b1acc-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1acc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1acc-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1acc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1acc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1acc-134">CommonParameters</span></span>
<span data-ttu-id="b1acc-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1acc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1acc-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1acc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1acc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b1acc-137">INPUTS</span></span>

### <span data-ttu-id="b1acc-138">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="b1acc-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b1acc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b1acc-139">OUTPUTS</span></span>

### <span data-ttu-id="b1acc-140">IDatabasePrincipal （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="b1acc-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="b1acc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b1acc-141">NOTES</span></span>

<span data-ttu-id="b1acc-142">別名</span><span class="sxs-lookup"><span data-stu-id="b1acc-142">ALIASES</span></span>

<span data-ttu-id="b1acc-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b1acc-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1acc-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b1acc-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1acc-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b1acc-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1acc-146">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b1acc-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1acc-147">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b1acc-148">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b1acc-149">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b1acc-150">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b1acc-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b1acc-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1acc-152">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="b1acc-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b1acc-153">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b1acc-154">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b1acc-155">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b1acc-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b1acc-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b1acc-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="b1acc-157">VALUE <IDatabasePrincipal [] >： Kusto 資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="b1acc-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="b1acc-158">`Name <String>`：資料庫主要名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="b1acc-159">`Role <DatabasePrincipalRole>`：資料庫主體角色。</span><span class="sxs-lookup"><span data-stu-id="b1acc-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="b1acc-160">`Type <DatabasePrincipalType>`：資料庫主體類型。</span><span class="sxs-lookup"><span data-stu-id="b1acc-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="b1acc-161">`[AppId <String>]`：應用程式識別碼-僅適用于應用程式主體類型。</span><span class="sxs-lookup"><span data-stu-id="b1acc-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="b1acc-162">`[Email <String>]`：資料庫主要電子郵件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b1acc-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="b1acc-163">`[Fqn <String>]`：資料庫主體的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="b1acc-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="b1acc-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1acc-164">RELATED LINKS</span></span>

