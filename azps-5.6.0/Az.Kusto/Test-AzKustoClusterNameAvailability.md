---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: dcc402b2db390403a6106953b3ecbdd6cc52a2b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902566"
---
# <span data-ttu-id="cd992-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cd992-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="cd992-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd992-102">SYNOPSIS</span></span>
<span data-ttu-id="cd992-103">檢查組名是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="cd992-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="cd992-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd992-104">SYNTAX</span></span>

### <span data-ttu-id="cd992-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cd992-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd992-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd992-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd992-107">描述</span><span class="sxs-lookup"><span data-stu-id="cd992-107">DESCRIPTION</span></span>
<span data-ttu-id="cd992-108">檢查組名是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="cd992-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="cd992-109">例子</span><span class="sxs-lookup"><span data-stu-id="cd992-109">EXAMPLES</span></span>

### <span data-ttu-id="cd992-110">範例 1：檢查使用中的 Kusto 組名可用性</span><span class="sxs-lookup"><span data-stu-id="cd992-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="cd992-111">上述命令會返回名稱為"testnewkustocluster"的 Kusto 叢集是否存在於「美國東部」地區。</span><span class="sxs-lookup"><span data-stu-id="cd992-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="cd992-112">範例 2：檢查未使用之 Kusto 組名的可用性</span><span class="sxs-lookup"><span data-stu-id="cd992-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="cd992-113">上述命令會返回名稱為「availablekustocluster」的 Kusto 叢集是否存在於「美國東部」地區。</span><span class="sxs-lookup"><span data-stu-id="cd992-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="cd992-114">參數</span><span class="sxs-lookup"><span data-stu-id="cd992-114">PARAMETERS</span></span>

### <span data-ttu-id="cd992-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd992-115">-DefaultProfile</span></span>
<span data-ttu-id="cd992-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd992-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd992-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd992-117">-InputObject</span></span>
<span data-ttu-id="cd992-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cd992-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd992-119">-位置</span><span class="sxs-lookup"><span data-stu-id="cd992-119">-Location</span></span>
<span data-ttu-id="cd992-120">Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="cd992-120">Azure location.</span></span>

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

### <span data-ttu-id="cd992-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd992-121">-Name</span></span>
<span data-ttu-id="cd992-122">組名。</span><span class="sxs-lookup"><span data-stu-id="cd992-122">Cluster name.</span></span>

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

### <span data-ttu-id="cd992-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd992-123">-SubscriptionId</span></span>
<span data-ttu-id="cd992-124">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cd992-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd992-125">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cd992-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd992-126">-類型</span><span class="sxs-lookup"><span data-stu-id="cd992-126">-Type</span></span>
<span data-ttu-id="cd992-127">資源類型，Microsoft.Kusto/clusters。</span><span class="sxs-lookup"><span data-stu-id="cd992-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="cd992-128">-確認</span><span class="sxs-lookup"><span data-stu-id="cd992-128">-Confirm</span></span>
<span data-ttu-id="cd992-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cd992-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd992-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd992-130">-WhatIf</span></span>
<span data-ttu-id="cd992-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd992-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd992-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd992-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd992-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd992-133">CommonParameters</span></span>
<span data-ttu-id="cd992-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd992-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd992-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd992-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd992-136">輸入</span><span class="sxs-lookup"><span data-stu-id="cd992-136">INPUTS</span></span>

### <span data-ttu-id="cd992-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cd992-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cd992-138">輸出</span><span class="sxs-lookup"><span data-stu-id="cd992-138">OUTPUTS</span></span>

### <span data-ttu-id="cd992-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="cd992-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="cd992-140">筆記</span><span class="sxs-lookup"><span data-stu-id="cd992-140">NOTES</span></span>

<span data-ttu-id="cd992-141">別名</span><span class="sxs-lookup"><span data-stu-id="cd992-141">ALIASES</span></span>

<span data-ttu-id="cd992-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cd992-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd992-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cd992-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd992-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cd992-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd992-145">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cd992-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd992-146">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd992-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cd992-147">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="cd992-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cd992-148">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd992-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cd992-149">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="cd992-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cd992-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="cd992-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd992-151">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="cd992-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cd992-152">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd992-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cd992-153">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cd992-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cd992-154">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cd992-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cd992-155">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cd992-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cd992-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd992-156">RELATED LINKS</span></span>

