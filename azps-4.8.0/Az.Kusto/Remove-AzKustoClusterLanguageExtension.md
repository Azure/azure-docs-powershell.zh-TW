---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970483"
---
# <span data-ttu-id="6e033-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="6e033-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="6e033-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e033-102">SYNOPSIS</span></span>
<span data-ttu-id="6e033-103">移除可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="6e033-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6e033-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e033-104">SYNTAX</span></span>

### <span data-ttu-id="6e033-105">RemoveExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6e033-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e033-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6e033-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e033-107">說明</span><span class="sxs-lookup"><span data-stu-id="6e033-107">DESCRIPTION</span></span>
<span data-ttu-id="6e033-108">移除可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="6e033-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6e033-109">示例</span><span class="sxs-lookup"><span data-stu-id="6e033-109">EXAMPLES</span></span>

### <span data-ttu-id="6e033-110">範例1：移除群集中的語言延伸清單</span><span class="sxs-lookup"><span data-stu-id="6e033-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="6e033-111">上述命令會移除可在 KQL 查詢中執行的語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="6e033-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6e033-112">參數</span><span class="sxs-lookup"><span data-stu-id="6e033-112">PARAMETERS</span></span>

### <span data-ttu-id="6e033-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e033-113">-AsJob</span></span>
<span data-ttu-id="6e033-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6e033-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6e033-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6e033-115">-ClusterName</span></span>
<span data-ttu-id="6e033-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6e033-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e033-117">-DefaultProfile</span></span>
<span data-ttu-id="6e033-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e033-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e033-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e033-119">-InputObject</span></span>
<span data-ttu-id="6e033-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6e033-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e033-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6e033-121">-NoWait</span></span>
<span data-ttu-id="6e033-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6e033-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e033-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e033-123">-PassThru</span></span>
<span data-ttu-id="6e033-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="6e033-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6e033-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e033-125">-ResourceGroupName</span></span>
<span data-ttu-id="6e033-126">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6e033-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e033-127">-SubscriptionId</span></span>
<span data-ttu-id="6e033-128">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6e033-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6e033-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6e033-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6e033-130">-值</span><span class="sxs-lookup"><span data-stu-id="6e033-130">-Value</span></span>
<span data-ttu-id="6e033-131">語言擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="6e033-131">The list of language extensions.</span></span>
<span data-ttu-id="6e033-132">若要建立，請參閱值屬性的記事區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6e033-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e033-133">-確認</span><span class="sxs-lookup"><span data-stu-id="6e033-133">-Confirm</span></span>
<span data-ttu-id="6e033-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e033-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e033-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e033-135">-WhatIf</span></span>
<span data-ttu-id="6e033-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e033-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e033-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e033-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e033-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e033-138">CommonParameters</span></span>
<span data-ttu-id="6e033-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e033-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e033-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6e033-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e033-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6e033-141">INPUTS</span></span>

### <span data-ttu-id="6e033-142">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="6e033-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6e033-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6e033-143">OUTPUTS</span></span>

### <span data-ttu-id="6e033-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6e033-144">System.Boolean</span></span>

## <span data-ttu-id="6e033-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6e033-145">NOTES</span></span>

<span data-ttu-id="6e033-146">別名</span><span class="sxs-lookup"><span data-stu-id="6e033-146">ALIASES</span></span>

<span data-ttu-id="6e033-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6e033-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e033-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6e033-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e033-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6e033-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e033-150">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6e033-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e033-151">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6e033-152">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6e033-153">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6e033-154">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6e033-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="6e033-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e033-156">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="6e033-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6e033-157">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6e033-158">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6e033-159">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6e033-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6e033-160">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6e033-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="6e033-161">VALUE <ILanguageExtension [] >：語言延伸清單。</span><span class="sxs-lookup"><span data-stu-id="6e033-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="6e033-162">`[Name <LanguageExtensionName?>]`：語言副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="6e033-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="6e033-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e033-163">RELATED LINKS</span></span>

