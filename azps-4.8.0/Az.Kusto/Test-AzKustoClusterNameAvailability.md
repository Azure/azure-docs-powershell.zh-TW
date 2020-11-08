---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127793"
---
# <span data-ttu-id="8c42f-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8c42f-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="8c42f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c42f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c42f-103">檢查群集名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="8c42f-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="8c42f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c42f-104">SYNTAX</span></span>

### <span data-ttu-id="8c42f-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8c42f-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c42f-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8c42f-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c42f-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c42f-107">DESCRIPTION</span></span>
<span data-ttu-id="8c42f-108">檢查群集名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="8c42f-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="8c42f-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c42f-109">EXAMPLES</span></span>

### <span data-ttu-id="8c42f-110">範例1：檢查使用中的 Kusto 群集名稱是否有空？</span><span class="sxs-lookup"><span data-stu-id="8c42f-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="8c42f-111">上述命令會傳回名為 "testnewkustocluster" 的 Kusto 群集是否存在於 "東 US" 區域中。</span><span class="sxs-lookup"><span data-stu-id="8c42f-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="8c42f-112">範例2：檢查是否有空使用中的 Kusto 群集名稱</span><span class="sxs-lookup"><span data-stu-id="8c42f-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="8c42f-113">上述命令會傳回名為 "availablekustocluster" 的 Kusto 群集是否存在於 "東 US" 區域中。</span><span class="sxs-lookup"><span data-stu-id="8c42f-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="8c42f-114">參數</span><span class="sxs-lookup"><span data-stu-id="8c42f-114">PARAMETERS</span></span>

### <span data-ttu-id="8c42f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c42f-115">-DefaultProfile</span></span>
<span data-ttu-id="8c42f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c42f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c42f-117">-InputObject</span></span>
<span data-ttu-id="8c42f-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8c42f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c42f-119">-位置</span><span class="sxs-lookup"><span data-stu-id="8c42f-119">-Location</span></span>
<span data-ttu-id="8c42f-120">Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="8c42f-120">Azure location.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c42f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c42f-121">-Name</span></span>
<span data-ttu-id="8c42f-122">[群集名稱]。</span><span class="sxs-lookup"><span data-stu-id="8c42f-122">Cluster name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c42f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c42f-123">-SubscriptionId</span></span>
<span data-ttu-id="8c42f-124">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8c42f-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c42f-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8c42f-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c42f-126">-類型</span><span class="sxs-lookup"><span data-stu-id="8c42f-126">-Type</span></span>
<span data-ttu-id="8c42f-127">Kusto/群集的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8c42f-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c42f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8c42f-128">-Confirm</span></span>
<span data-ttu-id="8c42f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c42f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c42f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c42f-130">-WhatIf</span></span>
<span data-ttu-id="8c42f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c42f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c42f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c42f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c42f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c42f-133">CommonParameters</span></span>
<span data-ttu-id="8c42f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c42f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c42f-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c42f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c42f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8c42f-136">INPUTS</span></span>

### <span data-ttu-id="8c42f-137">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="8c42f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8c42f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8c42f-138">OUTPUTS</span></span>

### <span data-ttu-id="8c42f-139">ICheckNameResult （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="8c42f-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="8c42f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8c42f-140">NOTES</span></span>

<span data-ttu-id="8c42f-141">別名</span><span class="sxs-lookup"><span data-stu-id="8c42f-141">ALIASES</span></span>

<span data-ttu-id="8c42f-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8c42f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c42f-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8c42f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c42f-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8c42f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c42f-145">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8c42f-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c42f-146">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8c42f-147">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8c42f-148">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8c42f-149">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8c42f-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8c42f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c42f-151">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="8c42f-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8c42f-152">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8c42f-153">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c42f-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8c42f-154">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8c42f-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8c42f-155">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8c42f-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8c42f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c42f-156">RELATED LINKS</span></span>

