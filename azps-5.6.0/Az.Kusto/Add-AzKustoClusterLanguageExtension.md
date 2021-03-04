---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 0e1cfc142c4c98614519c26639144cc701d2118c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905070"
---
# <span data-ttu-id="ba6a1-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="ba6a1-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="ba6a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6a1-103">新增可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ba6a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba6a1-104">SYNTAX</span></span>

### <span data-ttu-id="ba6a1-105">AddExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="ba6a1-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba6a1-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ba6a1-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba6a1-107">描述</span><span class="sxs-lookup"><span data-stu-id="ba6a1-107">DESCRIPTION</span></span>
<span data-ttu-id="ba6a1-108">新增可在 KQL 查詢內執行的語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ba6a1-109">例子</span><span class="sxs-lookup"><span data-stu-id="ba6a1-109">EXAMPLES</span></span>

### <span data-ttu-id="ba6a1-110">範例 1：新增語言延伸模組清單</span><span class="sxs-lookup"><span data-stu-id="ba6a1-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="ba6a1-111">上述命令會新增可在 KQL 查詢中執行的語言延伸模組清單</span><span class="sxs-lookup"><span data-stu-id="ba6a1-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="ba6a1-112">參數</span><span class="sxs-lookup"><span data-stu-id="ba6a1-112">PARAMETERS</span></span>

### <span data-ttu-id="ba6a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba6a1-113">-AsJob</span></span>
<span data-ttu-id="ba6a1-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="ba6a1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ba6a1-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba6a1-115">-ClusterName</span></span>
<span data-ttu-id="ba6a1-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba6a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6a1-117">-DefaultProfile</span></span>
<span data-ttu-id="ba6a1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba6a1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba6a1-119">-InputObject</span></span>
<span data-ttu-id="ba6a1-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba6a1-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba6a1-121">-NoWait</span></span>
<span data-ttu-id="ba6a1-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="ba6a1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba6a1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba6a1-123">-PassThru</span></span>
<span data-ttu-id="ba6a1-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="ba6a1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba6a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba6a1-126">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba6a1-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba6a1-127">-SubscriptionId</span></span>
<span data-ttu-id="ba6a1-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba6a1-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba6a1-130">-值</span><span class="sxs-lookup"><span data-stu-id="ba6a1-130">-Value</span></span>
<span data-ttu-id="ba6a1-131">語言延伸模組清單。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-131">The list of language extensions.</span></span>
<span data-ttu-id="ba6a1-132">若要建構，請參閱 VALUE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba6a1-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ba6a1-133">-Confirm</span></span>
<span data-ttu-id="ba6a1-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6a1-135">-WhatIf</span></span>
<span data-ttu-id="ba6a1-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6a1-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6a1-138">CommonParameters</span></span>
<span data-ttu-id="ba6a1-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6a1-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba6a1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6a1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ba6a1-141">INPUTS</span></span>

### <span data-ttu-id="ba6a1-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ba6a1-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ba6a1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ba6a1-143">OUTPUTS</span></span>

### <span data-ttu-id="ba6a1-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba6a1-144">System.Boolean</span></span>

## <span data-ttu-id="ba6a1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ba6a1-145">NOTES</span></span>

<span data-ttu-id="ba6a1-146">別名</span><span class="sxs-lookup"><span data-stu-id="ba6a1-146">ALIASES</span></span>

<span data-ttu-id="ba6a1-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ba6a1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba6a1-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba6a1-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba6a1-150">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ba6a1-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba6a1-151">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ba6a1-152">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ba6a1-153">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ba6a1-154">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ba6a1-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="ba6a1-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba6a1-156">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ba6a1-157">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ba6a1-158">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ba6a1-159">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ba6a1-160">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ba6a1-161">VALUE <ILanguageExtension[]>：語言副檔名清單。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ba6a1-162">`[Name <LanguageExtensionName?>]`：語言副檔名。</span><span class="sxs-lookup"><span data-stu-id="ba6a1-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="ba6a1-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba6a1-163">RELATED LINKS</span></span>

