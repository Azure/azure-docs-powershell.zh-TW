---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: febe9b4c758fb96e37962d810ef765b66b79fd24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906406"
---
# <span data-ttu-id="6553d-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="6553d-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="6553d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6553d-102">SYNOPSIS</span></span>
<span data-ttu-id="6553d-103">取得 IoT 安全性匯總提醒</span><span class="sxs-lookup"><span data-stu-id="6553d-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="6553d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6553d-104">SYNTAX</span></span>

### <span data-ttu-id="6553d-105">SolutionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="6553d-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6553d-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="6553d-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6553d-107">描述</span><span class="sxs-lookup"><span data-stu-id="6553d-107">DESCRIPTION</span></span>
<span data-ttu-id="6553d-108">Cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert iot 中樞裝置上，會返回一或多個匯總通知。</span><span class="sxs-lookup"><span data-stu-id="6553d-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="6553d-109">匯總警示的名稱是警示類型和警示被打平的日期組合，以 '/' 分隔。</span><span class="sxs-lookup"><span data-stu-id="6553d-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="6553d-110">例子</span><span class="sxs-lookup"><span data-stu-id="6553d-110">EXAMPLES</span></span>

### <span data-ttu-id="6553d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6553d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="6553d-112">取得匯總警示 "IoT_Bruteforce_Fail/2019-02-02" (名稱結合來自警示類型及其匯總日期) 的解決方案 "MySolution" 和資源群組 "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="6553d-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="6553d-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="6553d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="6553d-114">取得解決方案 "MySolution" 和資源群組 "MyResourceGroup" 中所有匯總通知的清單</span><span class="sxs-lookup"><span data-stu-id="6553d-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="6553d-115">參數</span><span class="sxs-lookup"><span data-stu-id="6553d-115">PARAMETERS</span></span>

### <span data-ttu-id="6553d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6553d-116">-DefaultProfile</span></span>
<span data-ttu-id="6553d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6553d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6553d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6553d-118">-Name</span></span>
<span data-ttu-id="6553d-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6553d-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6553d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6553d-120">-ResourceGroupName</span></span>
<span data-ttu-id="6553d-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6553d-121">Resource group name.</span></span>

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

### <span data-ttu-id="6553d-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="6553d-122">-SolutionName</span></span>
<span data-ttu-id="6553d-123">解決方案名稱</span><span class="sxs-lookup"><span data-stu-id="6553d-123">Solution name</span></span>

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

### <span data-ttu-id="6553d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6553d-124">CommonParameters</span></span>
<span data-ttu-id="6553d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6553d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6553d-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6553d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6553d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6553d-127">INPUTS</span></span>

### <span data-ttu-id="6553d-128">沒有</span><span class="sxs-lookup"><span data-stu-id="6553d-128">None</span></span>

## <span data-ttu-id="6553d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6553d-129">OUTPUTS</span></span>

### <span data-ttu-id="6553d-130">Microsoft.Azure.Commands.Security.models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="6553d-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="6553d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6553d-131">NOTES</span></span>

## <span data-ttu-id="6553d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6553d-132">RELATED LINKS</span></span>
