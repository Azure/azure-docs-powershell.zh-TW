---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f4be2a5da2dc8455b6e6674e7e74050ea506ae0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910053"
---
# <span data-ttu-id="e46da-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="e46da-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="e46da-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e46da-102">SYNOPSIS</span></span>
<span data-ttu-id="e46da-103">會取回使用者解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="e46da-104">語法</span><span class="sxs-lookup"><span data-stu-id="e46da-104">SYNTAX</span></span>

### <span data-ttu-id="e46da-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="e46da-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e46da-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e46da-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e46da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e46da-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e46da-108">清單</span><span class="sxs-lookup"><span data-stu-id="e46da-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e46da-109">描述</span><span class="sxs-lookup"><span data-stu-id="e46da-109">DESCRIPTION</span></span>
<span data-ttu-id="e46da-110">會取回使用者解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="e46da-111">例子</span><span class="sxs-lookup"><span data-stu-id="e46da-111">EXAMPLES</span></span>

### <span data-ttu-id="e46da-112">範例 1：根據名稱取得監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="e46da-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e46da-113">此命令會按名稱獲得監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="e46da-114">範例 2：根據資源識別碼取得監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="e46da-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="e46da-115">此命令會以資源識別碼獲得監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="e46da-116">範例 3：根據物件取得監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="e46da-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e46da-117">此命令會按物件獲得監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="e46da-118">範例 4：在資源群組下取得所有監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="e46da-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e46da-119">此命令會獲得資源群組下的所有監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="e46da-120">範例 5：在訂閱下取得所有監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="e46da-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e46da-121">此命令會獲得訂閱下的所有監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="e46da-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="e46da-122">參數</span><span class="sxs-lookup"><span data-stu-id="e46da-122">PARAMETERS</span></span>

### <span data-ttu-id="e46da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46da-123">-DefaultProfile</span></span>
<span data-ttu-id="e46da-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e46da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46da-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46da-125">-InputObject</span></span>
<span data-ttu-id="e46da-126">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e46da-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e46da-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e46da-127">-Name</span></span>
<span data-ttu-id="e46da-128">使用者解決方案名稱。</span><span class="sxs-lookup"><span data-stu-id="e46da-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46da-129">-ResourceGroupName</span></span>
<span data-ttu-id="e46da-130">要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e46da-130">The name of the resource group to get.</span></span>
<span data-ttu-id="e46da-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e46da-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46da-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e46da-132">-SubscriptionId</span></span>
<span data-ttu-id="e46da-133">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e46da-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e46da-134">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e46da-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46da-135">CommonParameters</span></span>
<span data-ttu-id="e46da-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e46da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46da-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e46da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46da-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e46da-138">INPUTS</span></span>

### <span data-ttu-id="e46da-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="e46da-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="e46da-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e46da-140">OUTPUTS</span></span>

### <span data-ttu-id="e46da-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="e46da-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="e46da-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e46da-142">NOTES</span></span>

<span data-ttu-id="e46da-143">別名</span><span class="sxs-lookup"><span data-stu-id="e46da-143">ALIASES</span></span>

<span data-ttu-id="e46da-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e46da-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e46da-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e46da-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e46da-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e46da-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e46da-147">INPUTOBJECT： <IMonitoringSolutionsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e46da-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e46da-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e46da-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e46da-149">`[ManagementAssociationName <String>]`：User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="e46da-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="e46da-150">`[ManagementConfigurationName <String>]`：使用者管理組組名。</span><span class="sxs-lookup"><span data-stu-id="e46da-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="e46da-151">`[ProviderName <String>]`：父資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="e46da-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="e46da-152">`[ResourceGroupName <String>]`：要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e46da-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="e46da-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e46da-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="e46da-154">`[ResourceName <String>]`：父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e46da-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="e46da-155">`[ResourceType <String>]`：父資源的資源類型</span><span class="sxs-lookup"><span data-stu-id="e46da-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="e46da-156">`[SolutionName <String>]`：使用者解決方案名稱。</span><span class="sxs-lookup"><span data-stu-id="e46da-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="e46da-157">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e46da-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e46da-158">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e46da-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e46da-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="e46da-159">RELATED LINKS</span></span>

