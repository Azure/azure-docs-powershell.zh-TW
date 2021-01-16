---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282006"
---
# <span data-ttu-id="093f9-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="093f9-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="093f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="093f9-102">SYNOPSIS</span></span>
<span data-ttu-id="093f9-103">新增可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="093f9-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="093f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="093f9-104">SYNTAX</span></span>

### <span data-ttu-id="093f9-105">AddExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="093f9-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="093f9-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="093f9-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="093f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="093f9-107">DESCRIPTION</span></span>
<span data-ttu-id="093f9-108">新增可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="093f9-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="093f9-109">示例</span><span class="sxs-lookup"><span data-stu-id="093f9-109">EXAMPLES</span></span>

### <span data-ttu-id="093f9-110">範例1：新增語言延伸清單</span><span class="sxs-lookup"><span data-stu-id="093f9-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="093f9-111">上述命令會新增可在 KQL 查詢中執行的語言延伸清單</span><span class="sxs-lookup"><span data-stu-id="093f9-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="093f9-112">參數</span><span class="sxs-lookup"><span data-stu-id="093f9-112">PARAMETERS</span></span>

### <span data-ttu-id="093f9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="093f9-113">-AsJob</span></span>
<span data-ttu-id="093f9-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="093f9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="093f9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="093f9-115">-ClusterName</span></span>
<span data-ttu-id="093f9-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="093f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093f9-117">-DefaultProfile</span></span>
<span data-ttu-id="093f9-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="093f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="093f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="093f9-119">-InputObject</span></span>
<span data-ttu-id="093f9-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="093f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="093f9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="093f9-121">-NoWait</span></span>
<span data-ttu-id="093f9-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="093f9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="093f9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="093f9-123">-PassThru</span></span>
<span data-ttu-id="093f9-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="093f9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="093f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="093f9-126">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="093f9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="093f9-127">-SubscriptionId</span></span>
<span data-ttu-id="093f9-128">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="093f9-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="093f9-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="093f9-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="093f9-130">-值</span><span class="sxs-lookup"><span data-stu-id="093f9-130">-Value</span></span>
<span data-ttu-id="093f9-131">語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="093f9-131">The list of language extensions.</span></span>
<span data-ttu-id="093f9-132">若要建立，請參閱值屬性的記事區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="093f9-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093f9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="093f9-133">-Confirm</span></span>
<span data-ttu-id="093f9-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="093f9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093f9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093f9-135">-WhatIf</span></span>
<span data-ttu-id="093f9-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="093f9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="093f9-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="093f9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093f9-138">CommonParameters</span></span>
<span data-ttu-id="093f9-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="093f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093f9-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="093f9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093f9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="093f9-141">INPUTS</span></span>

### <span data-ttu-id="093f9-142">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="093f9-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="093f9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="093f9-143">OUTPUTS</span></span>

### <span data-ttu-id="093f9-144">System.object</span><span class="sxs-lookup"><span data-stu-id="093f9-144">System.Boolean</span></span>

## <span data-ttu-id="093f9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="093f9-145">NOTES</span></span>

<span data-ttu-id="093f9-146">別名</span><span class="sxs-lookup"><span data-stu-id="093f9-146">ALIASES</span></span>

<span data-ttu-id="093f9-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="093f9-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="093f9-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="093f9-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="093f9-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="093f9-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="093f9-150">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="093f9-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="093f9-151">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="093f9-152">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="093f9-153">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="093f9-154">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="093f9-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="093f9-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="093f9-156">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="093f9-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="093f9-157">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="093f9-158">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="093f9-159">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="093f9-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="093f9-160">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="093f9-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="093f9-161">VALUE <ILanguageExtension [] >：語言延伸清單。</span><span class="sxs-lookup"><span data-stu-id="093f9-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="093f9-162">`[Name <LanguageExtensionName?>]`：語言副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="093f9-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="093f9-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="093f9-163">RELATED LINKS</span></span>

