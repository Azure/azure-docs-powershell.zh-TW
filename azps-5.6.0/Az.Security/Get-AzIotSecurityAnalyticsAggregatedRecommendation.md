---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: f57d3b3eb254a547059cb2e7c37a0720ee5f6310
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906405"
---
# <span data-ttu-id="f2793-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="f2793-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="f2793-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2793-102">SYNOPSIS</span></span>
<span data-ttu-id="f2793-103">取得 IoT 安全性匯總建議</span><span class="sxs-lookup"><span data-stu-id="f2793-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="f2793-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2793-104">SYNTAX</span></span>

### <span data-ttu-id="f2793-105">SolutionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="f2793-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2793-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f2793-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2793-107">描述</span><span class="sxs-lookup"><span data-stu-id="f2793-107">DESCRIPTION</span></span>
<span data-ttu-id="f2793-108">Cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert iot 中樞裝置上，會返回一或多個匯總建議。</span><span class="sxs-lookup"><span data-stu-id="f2793-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="f2793-109">匯總建議的名稱是它的類型</span><span class="sxs-lookup"><span data-stu-id="f2793-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="f2793-110">例子</span><span class="sxs-lookup"><span data-stu-id="f2793-110">EXAMPLES</span></span>

### <span data-ttu-id="f2793-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2793-111">Example 1</span></span>
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

<span data-ttu-id="f2793-112">在安全性解決方案 "MySolution" IoT_OpenPorts資源群組 "MyResourceGroup" 中取得匯總建議 "IoT_OpenPorts"</span><span class="sxs-lookup"><span data-stu-id="f2793-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="f2793-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f2793-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="f2793-114">在安全性解決方案 「MySolution」和資源群組 「MyResourceGroup」中取得匯總建議清單</span><span class="sxs-lookup"><span data-stu-id="f2793-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="f2793-115">參數</span><span class="sxs-lookup"><span data-stu-id="f2793-115">PARAMETERS</span></span>

### <span data-ttu-id="f2793-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2793-116">-DefaultProfile</span></span>
<span data-ttu-id="f2793-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2793-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2793-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2793-118">-Name</span></span>
<span data-ttu-id="f2793-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f2793-119">Resource name.</span></span>

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

### <span data-ttu-id="f2793-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2793-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2793-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2793-121">Resource group name.</span></span>

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

### <span data-ttu-id="f2793-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="f2793-122">-SolutionName</span></span>
<span data-ttu-id="f2793-123">解決方案名稱</span><span class="sxs-lookup"><span data-stu-id="f2793-123">Solution name</span></span>

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

### <span data-ttu-id="f2793-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2793-124">CommonParameters</span></span>
<span data-ttu-id="f2793-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2793-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2793-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2793-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2793-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f2793-127">INPUTS</span></span>

### <span data-ttu-id="f2793-128">沒有</span><span class="sxs-lookup"><span data-stu-id="f2793-128">None</span></span>

## <span data-ttu-id="f2793-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f2793-129">OUTPUTS</span></span>

### <span data-ttu-id="f2793-130">Microsoft.Azure.Commands.Security.models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="f2793-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="f2793-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f2793-131">NOTES</span></span>

## <span data-ttu-id="f2793-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2793-132">RELATED LINKS</span></span>
