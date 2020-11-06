---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614132"
---
# <span data-ttu-id="20feb-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="20feb-101">Get-AzAlert</span></span>

## <span data-ttu-id="20feb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20feb-102">SYNOPSIS</span></span>
<span data-ttu-id="20feb-103">取得提醒資訊</span><span class="sxs-lookup"><span data-stu-id="20feb-103">Get Alerts Information</span></span>

## <span data-ttu-id="20feb-104">句法</span><span class="sxs-lookup"><span data-stu-id="20feb-104">SYNTAX</span></span>

### <span data-ttu-id="20feb-105">AlertsListByFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="20feb-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20feb-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="20feb-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20feb-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="20feb-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20feb-108">說明</span><span class="sxs-lookup"><span data-stu-id="20feb-108">DESCRIPTION</span></span>
<span data-ttu-id="20feb-109">**AzAlert** Cmdlet 會觸發警報實例。</span><span class="sxs-lookup"><span data-stu-id="20feb-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="20feb-110">示例</span><span class="sxs-lookup"><span data-stu-id="20feb-110">EXAMPLES</span></span>

### <span data-ttu-id="20feb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="20feb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="20feb-112">使用 Sev2 嚴重度及激發的監視器條件列出所有警示。</span><span class="sxs-lookup"><span data-stu-id="20feb-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="20feb-113">將 IncludeCoNtext 設定為 true，包括自訂的警示負載。</span><span class="sxs-lookup"><span data-stu-id="20feb-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="20feb-114">使用 Format-List 取得清單中每個警示的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="20feb-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="20feb-115">範例2</span><span class="sxs-lookup"><span data-stu-id="20feb-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="20feb-116">透過識別碼 (GUID) 或資源識別碼 (完整 ARM Id 取得警報詳細資料) </span><span class="sxs-lookup"><span data-stu-id="20feb-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="20feb-117">參數</span><span class="sxs-lookup"><span data-stu-id="20feb-117">PARAMETERS</span></span>

### <span data-ttu-id="20feb-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="20feb-118">-AlertId</span></span>
<span data-ttu-id="20feb-119">警示/警示的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="20feb-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="20feb-120">-AlertRuleId</span></span>
<span data-ttu-id="20feb-121">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="20feb-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="20feb-122">-CustomTimeRange</span></span>
<span data-ttu-id="20feb-123">支援的格式- \< \> / \< \> 在時間為 ISO-8601 格式時的開始時間結束時間</span><span class="sxs-lookup"><span data-stu-id="20feb-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20feb-124">-DefaultProfile</span></span>
<span data-ttu-id="20feb-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20feb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-126">-IncludeCoNtext</span><span class="sxs-lookup"><span data-stu-id="20feb-126">-IncludeContext</span></span>
<span data-ttu-id="20feb-127">包含內容 (自訂的負載) 警報</span><span class="sxs-lookup"><span data-stu-id="20feb-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="20feb-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="20feb-129">包括 EgressConfig</span><span class="sxs-lookup"><span data-stu-id="20feb-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="20feb-130">-MonitorCondition</span></span>
<span data-ttu-id="20feb-131">篩選監視器條件</span><span class="sxs-lookup"><span data-stu-id="20feb-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="20feb-132">-MonitorService</span></span>
<span data-ttu-id="20feb-133">篩選 Moniter 服務</span><span class="sxs-lookup"><span data-stu-id="20feb-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="20feb-134">-PageCount</span></span>
<span data-ttu-id="20feb-135">要在頁面中回遷的警示數目。</span><span class="sxs-lookup"><span data-stu-id="20feb-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-136">-選取</span><span class="sxs-lookup"><span data-stu-id="20feb-136">-Select</span></span>
<span data-ttu-id="20feb-137">從基本版將必要的欄位投影出來。</span><span class="sxs-lookup"><span data-stu-id="20feb-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="20feb-138">預期的輸入是以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="20feb-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-139">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="20feb-139">-Severity</span></span>
<span data-ttu-id="20feb-140">在警示嚴重度篩選</span><span class="sxs-lookup"><span data-stu-id="20feb-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="20feb-141">-SmartGroupId</span></span>
<span data-ttu-id="20feb-142">篩選具有智慧群組識別碼的所有警示</span><span class="sxs-lookup"><span data-stu-id="20feb-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="20feb-143">-SortBy</span></span>
<span data-ttu-id="20feb-144">排序時要使用的警示屬性</span><span class="sxs-lookup"><span data-stu-id="20feb-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="20feb-145">-SortOrder</span></span>
<span data-ttu-id="20feb-146">排序次序</span><span class="sxs-lookup"><span data-stu-id="20feb-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-147">-State</span><span class="sxs-lookup"><span data-stu-id="20feb-147">-State</span></span>
<span data-ttu-id="20feb-148">篩選警示狀態</span><span class="sxs-lookup"><span data-stu-id="20feb-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20feb-149">-TargetResourceGroup</span></span>
<span data-ttu-id="20feb-150">篩選 [警示] 目標資源的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="20feb-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="20feb-151">-TargetResourceId</span></span>
<span data-ttu-id="20feb-152">篩選警報目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="20feb-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="20feb-153">-TargetResourceType</span></span>
<span data-ttu-id="20feb-154">篩選警報目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="20feb-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="20feb-155">-TimeRange</span></span>
<span data-ttu-id="20feb-156">支援的時間範圍值-1h、1d、7d、30d (預設為 1d) </span><span class="sxs-lookup"><span data-stu-id="20feb-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20feb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20feb-157">CommonParameters</span></span>
<span data-ttu-id="20feb-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20feb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20feb-159">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="20feb-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20feb-160">輸入</span><span class="sxs-lookup"><span data-stu-id="20feb-160">INPUTS</span></span>

### <span data-ttu-id="20feb-161">所有</span><span class="sxs-lookup"><span data-stu-id="20feb-161">None</span></span>

## <span data-ttu-id="20feb-162">輸出</span><span class="sxs-lookup"><span data-stu-id="20feb-162">OUTPUTS</span></span>

### <span data-ttu-id="20feb-163">AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="20feb-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="20feb-164">筆記</span><span class="sxs-lookup"><span data-stu-id="20feb-164">NOTES</span></span>

## <span data-ttu-id="20feb-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="20feb-165">RELATED LINKS</span></span>
