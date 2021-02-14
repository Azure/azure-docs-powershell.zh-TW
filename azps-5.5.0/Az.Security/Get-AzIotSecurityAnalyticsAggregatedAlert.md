---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127194"
---
# <span data-ttu-id="bb40e-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="bb40e-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="bb40e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb40e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb40e-103">取得 IoT 安全性匯總通知</span><span class="sxs-lookup"><span data-stu-id="bb40e-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="bb40e-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb40e-104">SYNTAX</span></span>

### <span data-ttu-id="bb40e-105">SolutionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="bb40e-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb40e-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="bb40e-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb40e-107">說明</span><span class="sxs-lookup"><span data-stu-id="bb40e-107">DESCRIPTION</span></span>
<span data-ttu-id="bb40e-108">Get-AzIotSecurityAnalyticsAggregatedAlert Cmdlet 會在 iot 中樞的裝置上傳回一或多個匯總警示。</span><span class="sxs-lookup"><span data-stu-id="bb40e-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="bb40e-109">[匯總警示] 的名稱是 [警示類型] 與 [警示 aggragted 日期] 的組合，並以 "/" 分隔。</span><span class="sxs-lookup"><span data-stu-id="bb40e-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="bb40e-110">示例</span><span class="sxs-lookup"><span data-stu-id="bb40e-110">EXAMPLES</span></span>

### <span data-ttu-id="bb40e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bb40e-111">Example 1</span></span>
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

<span data-ttu-id="bb40e-112">取得匯總警示「IoT_Bruteforce_Fail/2019-02-02 " (從警報類型和其匯總日期) 在方案" MySolution "和資源群組" MyResourceGroup "中結合的名稱</span><span class="sxs-lookup"><span data-stu-id="bb40e-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="bb40e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="bb40e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="bb40e-114">在解決方案 "MySolution" 和資源群組 "MyResourceGroup" 中取得所有匯總通知的清單</span><span class="sxs-lookup"><span data-stu-id="bb40e-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="bb40e-115">參數</span><span class="sxs-lookup"><span data-stu-id="bb40e-115">PARAMETERS</span></span>

### <span data-ttu-id="bb40e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb40e-116">-DefaultProfile</span></span>
<span data-ttu-id="bb40e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb40e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb40e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb40e-118">-Name</span></span>
<span data-ttu-id="bb40e-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bb40e-119">Resource name.</span></span>

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

### <span data-ttu-id="bb40e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb40e-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb40e-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bb40e-121">Resource group name.</span></span>

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

### <span data-ttu-id="bb40e-122">-解決方案名稱</span><span class="sxs-lookup"><span data-stu-id="bb40e-122">-SolutionName</span></span>
<span data-ttu-id="bb40e-123">方案名稱</span><span class="sxs-lookup"><span data-stu-id="bb40e-123">Solution name</span></span>

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

### <span data-ttu-id="bb40e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb40e-124">CommonParameters</span></span>
<span data-ttu-id="bb40e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb40e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb40e-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bb40e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb40e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bb40e-127">INPUTS</span></span>

### <span data-ttu-id="bb40e-128">所有</span><span class="sxs-lookup"><span data-stu-id="bb40e-128">None</span></span>

## <span data-ttu-id="bb40e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bb40e-129">OUTPUTS</span></span>

### <span data-ttu-id="bb40e-130">PSIoTSecurityAggregatedAlert 中的 IotSecuritySolutionAnalytics （Security..。</span><span class="sxs-lookup"><span data-stu-id="bb40e-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="bb40e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bb40e-131">NOTES</span></span>

## <span data-ttu-id="bb40e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb40e-132">RELATED LINKS</span></span>
