---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 6a687139f7dec156e539c09b864a88c4e8876fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907129"
---
# <span data-ttu-id="62e60-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="62e60-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="62e60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62e60-102">SYNOPSIS</span></span>
<span data-ttu-id="62e60-103">移除可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="62e60-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="62e60-104">語法</span><span class="sxs-lookup"><span data-stu-id="62e60-104">SYNTAX</span></span>

### <span data-ttu-id="62e60-105">RemoveExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="62e60-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62e60-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="62e60-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62e60-107">描述</span><span class="sxs-lookup"><span data-stu-id="62e60-107">DESCRIPTION</span></span>
<span data-ttu-id="62e60-108">移除可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="62e60-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="62e60-109">例子</span><span class="sxs-lookup"><span data-stu-id="62e60-109">EXAMPLES</span></span>

### <span data-ttu-id="62e60-110">範例 1：從組群移除語言延伸模組清單</span><span class="sxs-lookup"><span data-stu-id="62e60-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="62e60-111">上述命令會移除可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="62e60-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="62e60-112">參數</span><span class="sxs-lookup"><span data-stu-id="62e60-112">PARAMETERS</span></span>

### <span data-ttu-id="62e60-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e60-113">-AsJob</span></span>
<span data-ttu-id="62e60-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="62e60-114">Run the command as a job</span></span>

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

### <span data-ttu-id="62e60-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="62e60-115">-ClusterName</span></span>
<span data-ttu-id="62e60-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="62e60-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="62e60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e60-117">-DefaultProfile</span></span>
<span data-ttu-id="62e60-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62e60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e60-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62e60-119">-InputObject</span></span>
<span data-ttu-id="62e60-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="62e60-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="62e60-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="62e60-121">-NoWait</span></span>
<span data-ttu-id="62e60-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="62e60-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62e60-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62e60-123">-PassThru</span></span>
<span data-ttu-id="62e60-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="62e60-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="62e60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e60-125">-ResourceGroupName</span></span>
<span data-ttu-id="62e60-126">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="62e60-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="62e60-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62e60-127">-SubscriptionId</span></span>
<span data-ttu-id="62e60-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="62e60-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="62e60-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="62e60-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="62e60-130">-值</span><span class="sxs-lookup"><span data-stu-id="62e60-130">-Value</span></span>
<span data-ttu-id="62e60-131">語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="62e60-131">The list of language extensions.</span></span>
<span data-ttu-id="62e60-132">若要建構，請參閱 VALUE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="62e60-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e60-133">-確認</span><span class="sxs-lookup"><span data-stu-id="62e60-133">-Confirm</span></span>
<span data-ttu-id="62e60-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="62e60-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e60-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e60-135">-WhatIf</span></span>
<span data-ttu-id="62e60-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62e60-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e60-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62e60-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e60-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e60-138">CommonParameters</span></span>
<span data-ttu-id="62e60-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62e60-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e60-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62e60-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e60-141">輸入</span><span class="sxs-lookup"><span data-stu-id="62e60-141">INPUTS</span></span>

### <span data-ttu-id="62e60-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="62e60-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="62e60-143">輸出</span><span class="sxs-lookup"><span data-stu-id="62e60-143">OUTPUTS</span></span>

### <span data-ttu-id="62e60-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62e60-144">System.Boolean</span></span>

## <span data-ttu-id="62e60-145">筆記</span><span class="sxs-lookup"><span data-stu-id="62e60-145">NOTES</span></span>

<span data-ttu-id="62e60-146">別名</span><span class="sxs-lookup"><span data-stu-id="62e60-146">ALIASES</span></span>

<span data-ttu-id="62e60-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="62e60-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62e60-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="62e60-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62e60-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="62e60-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62e60-150">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="62e60-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62e60-151">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="62e60-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="62e60-152">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="62e60-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="62e60-153">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="62e60-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="62e60-154">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="62e60-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="62e60-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="62e60-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62e60-156">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="62e60-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="62e60-157">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="62e60-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="62e60-158">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="62e60-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="62e60-159">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="62e60-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="62e60-160">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="62e60-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="62e60-161">VALUE <ILanguageExtension[]>：語言副檔名清單。</span><span class="sxs-lookup"><span data-stu-id="62e60-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="62e60-162">`[Name <LanguageExtensionName?>]`：語言副檔名。</span><span class="sxs-lookup"><span data-stu-id="62e60-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="62e60-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="62e60-163">RELATED LINKS</span></span>

