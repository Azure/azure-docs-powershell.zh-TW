---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127729"
---
# <span data-ttu-id="a0da9-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="a0da9-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="a0da9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0da9-102">SYNOPSIS</span></span>
<span data-ttu-id="a0da9-103">檢索使用者方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="a0da9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0da9-104">SYNTAX</span></span>

### <span data-ttu-id="a0da9-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="a0da9-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0da9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a0da9-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0da9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a0da9-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0da9-108">清單</span><span class="sxs-lookup"><span data-stu-id="a0da9-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a0da9-109">說明</span><span class="sxs-lookup"><span data-stu-id="a0da9-109">DESCRIPTION</span></span>
<span data-ttu-id="a0da9-110">檢索使用者方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="a0da9-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0da9-111">EXAMPLES</span></span>

### <span data-ttu-id="a0da9-112">範例1：透過名稱取得監視記錄分析方案</span><span class="sxs-lookup"><span data-stu-id="a0da9-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a0da9-113">這個命令會依名稱取得監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="a0da9-114">範例2：透過資源識別碼取得監視記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="a0da9-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="a0da9-115">這個命令會透過資源識別碼取得監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="a0da9-116">範例3：透過物件取得監視記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="a0da9-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a0da9-117">這個命令會透過物件取得監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="a0da9-118">範例4：取得資源群組下的所有監視記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="a0da9-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a0da9-119">這個命令會取得資源群組下的所有監視記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="a0da9-120">範例5：取得訂閱下的所有監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="a0da9-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="a0da9-121">這個命令會取得訂閱下的所有監視器記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="a0da9-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="a0da9-122">參數</span><span class="sxs-lookup"><span data-stu-id="a0da9-122">PARAMETERS</span></span>

### <span data-ttu-id="a0da9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0da9-123">-DefaultProfile</span></span>
<span data-ttu-id="a0da9-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0da9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0da9-125">-InputObject</span></span>
<span data-ttu-id="a0da9-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a0da9-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0da9-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0da9-127">-Name</span></span>
<span data-ttu-id="a0da9-128">使用者方案名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-128">User Solution Name.</span></span>

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

### <span data-ttu-id="a0da9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0da9-129">-ResourceGroupName</span></span>
<span data-ttu-id="a0da9-130">要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-130">The name of the resource group to get.</span></span>
<span data-ttu-id="a0da9-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0da9-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a0da9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0da9-132">-SubscriptionId</span></span>
<span data-ttu-id="a0da9-133">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a0da9-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0da9-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a0da9-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0da9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0da9-135">CommonParameters</span></span>
<span data-ttu-id="a0da9-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0da9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0da9-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0da9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0da9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a0da9-138">INPUTS</span></span>

### <span data-ttu-id="a0da9-139">IMonitoringSolutionsIdentity （MonitoringSolutions）的</span><span class="sxs-lookup"><span data-stu-id="a0da9-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="a0da9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a0da9-140">OUTPUTS</span></span>

### <span data-ttu-id="a0da9-141">ISolution （MonitoringSolutions）。 Api20151101Preview。</span><span class="sxs-lookup"><span data-stu-id="a0da9-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="a0da9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a0da9-142">NOTES</span></span>

<span data-ttu-id="a0da9-143">別名</span><span class="sxs-lookup"><span data-stu-id="a0da9-143">ALIASES</span></span>

<span data-ttu-id="a0da9-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a0da9-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0da9-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a0da9-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0da9-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a0da9-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0da9-147">INPUTOBJECT <IMonitoringSolutionsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a0da9-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0da9-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a0da9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0da9-149">`[ManagementAssociationName <String>]`：使用者 ManagementAssociation 名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="a0da9-150">`[ManagementConfigurationName <String>]`：使用者管理配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="a0da9-151">`[ProviderName <String>]`：父資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="a0da9-152">`[ResourceGroupName <String>]`：要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="a0da9-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0da9-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="a0da9-154">`[ResourceName <String>]`：父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="a0da9-155">`[ResourceType <String>]`：父資源的資源類型</span><span class="sxs-lookup"><span data-stu-id="a0da9-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="a0da9-156">`[SolutionName <String>]`：使用者方案名稱。</span><span class="sxs-lookup"><span data-stu-id="a0da9-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="a0da9-157">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a0da9-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a0da9-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a0da9-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a0da9-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0da9-159">RELATED LINKS</span></span>

