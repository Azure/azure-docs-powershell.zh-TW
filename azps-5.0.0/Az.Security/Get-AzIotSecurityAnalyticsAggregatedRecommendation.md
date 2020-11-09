---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285792"
---
# <span data-ttu-id="7da0d-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="7da0d-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="7da0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7da0d-102">SYNOPSIS</span></span>
<span data-ttu-id="7da0d-103">取得 IoT 安全性匯總建議</span><span class="sxs-lookup"><span data-stu-id="7da0d-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="7da0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7da0d-104">SYNTAX</span></span>

### <span data-ttu-id="7da0d-105">SolutionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="7da0d-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da0d-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7da0d-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da0d-107">說明</span><span class="sxs-lookup"><span data-stu-id="7da0d-107">DESCRIPTION</span></span>
<span data-ttu-id="7da0d-108">Get-AzIotSecurityAnalyticsAggregatedAlert Cmdlet 會傳回 iot 中樞裝置上的一個或多個匯總建議。</span><span class="sxs-lookup"><span data-stu-id="7da0d-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="7da0d-109">匯總建議的名稱是其類型</span><span class="sxs-lookup"><span data-stu-id="7da0d-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="7da0d-110">示例</span><span class="sxs-lookup"><span data-stu-id="7da0d-110">EXAMPLES</span></span>

### <span data-ttu-id="7da0d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7da0d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="7da0d-112">在安全性方案 "MySolution" 和資源群組 "MyResourceGroup" 中取得匯總建議「IoT_OpenPorts」</span><span class="sxs-lookup"><span data-stu-id="7da0d-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="7da0d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7da0d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="7da0d-114">在安全性方案 "MySolution" 和資源群組 "MyResourceGroup" 中取得匯總建議清單</span><span class="sxs-lookup"><span data-stu-id="7da0d-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="7da0d-115">參數</span><span class="sxs-lookup"><span data-stu-id="7da0d-115">PARAMETERS</span></span>

### <span data-ttu-id="7da0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da0d-116">-DefaultProfile</span></span>
<span data-ttu-id="7da0d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7da0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da0d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7da0d-118">-Name</span></span>
<span data-ttu-id="7da0d-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7da0d-119">Resource name.</span></span>

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

### <span data-ttu-id="7da0d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da0d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7da0d-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7da0d-121">Resource group name.</span></span>

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

### <span data-ttu-id="7da0d-122">-解決方案名稱</span><span class="sxs-lookup"><span data-stu-id="7da0d-122">-SolutionName</span></span>
<span data-ttu-id="7da0d-123">方案名稱</span><span class="sxs-lookup"><span data-stu-id="7da0d-123">Solution name</span></span>

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

### <span data-ttu-id="7da0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da0d-124">CommonParameters</span></span>
<span data-ttu-id="7da0d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7da0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da0d-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7da0d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da0d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7da0d-127">INPUTS</span></span>

### <span data-ttu-id="7da0d-128">所有</span><span class="sxs-lookup"><span data-stu-id="7da0d-128">None</span></span>

## <span data-ttu-id="7da0d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7da0d-129">OUTPUTS</span></span>

### <span data-ttu-id="7da0d-130">PSIoTSecurityAggregatedRecommendation 中的 IotSecuritySolutionAnalytics （Security..。</span><span class="sxs-lookup"><span data-stu-id="7da0d-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="7da0d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7da0d-131">NOTES</span></span>

## <span data-ttu-id="7da0d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7da0d-132">RELATED LINKS</span></span>
