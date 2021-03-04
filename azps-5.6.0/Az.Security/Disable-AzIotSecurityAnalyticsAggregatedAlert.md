---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: c698c91f8b4115fb811ebcda41eaf43662f0bf08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910658"
---
# <span data-ttu-id="d176f-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="d176f-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="d176f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d176f-102">SYNOPSIS</span></span>
<span data-ttu-id="d176f-103">關閉 Iot 匯總提醒</span><span class="sxs-lookup"><span data-stu-id="d176f-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="d176f-104">語法</span><span class="sxs-lookup"><span data-stu-id="d176f-104">SYNTAX</span></span>

### <span data-ttu-id="d176f-105">SolutionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d176f-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d176f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d176f-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d176f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d176f-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d176f-108">描述</span><span class="sxs-lookup"><span data-stu-id="d176f-108">DESCRIPTION</span></span>
<span data-ttu-id="d176f-109">此Disable-AzIotSecurityAnalyticsAggregatedAlert Cmdlet 會解除 iot 中樞裝置上特定的退格警示。</span><span class="sxs-lookup"><span data-stu-id="d176f-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="d176f-110">匯總警示的名稱是警示類型和警示被打平的日期組合，以 '/' 分隔。</span><span class="sxs-lookup"><span data-stu-id="d176f-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="d176f-111">例子</span><span class="sxs-lookup"><span data-stu-id="d176f-111">EXAMPLES</span></span>

### <span data-ttu-id="d176f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d176f-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="d176f-113">從通知類型及其匯總日期 (中結合的匯總警示 "IoT_SucessfulLocalLogin/2020-03-15") 從資源群組 "MyResourceGroup" 的 IoT 安全性解決方案 "MySolutionName" 關閉</span><span class="sxs-lookup"><span data-stu-id="d176f-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="d176f-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d176f-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="d176f-115">關閉使用資源識別碼 "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15" 的匯總通知</span><span class="sxs-lookup"><span data-stu-id="d176f-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="d176f-116">參數</span><span class="sxs-lookup"><span data-stu-id="d176f-116">PARAMETERS</span></span>

### <span data-ttu-id="d176f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d176f-117">-DefaultProfile</span></span>
<span data-ttu-id="d176f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d176f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d176f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d176f-119">-InputObject</span></span>
<span data-ttu-id="d176f-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d176f-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d176f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d176f-121">-Name</span></span>
<span data-ttu-id="d176f-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d176f-122">Resource name.</span></span>

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

### <span data-ttu-id="d176f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d176f-123">-PassThru</span></span>
<span data-ttu-id="d176f-124">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="d176f-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d176f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d176f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d176f-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d176f-126">Resource group name.</span></span>

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

### <span data-ttu-id="d176f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d176f-127">-ResourceId</span></span>
<span data-ttu-id="d176f-128">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d176f-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d176f-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="d176f-129">-SolutionName</span></span>
<span data-ttu-id="d176f-130">解決方案名稱</span><span class="sxs-lookup"><span data-stu-id="d176f-130">Solution name</span></span>

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

### <span data-ttu-id="d176f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d176f-131">-Confirm</span></span>
<span data-ttu-id="d176f-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d176f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d176f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d176f-133">-WhatIf</span></span>
<span data-ttu-id="d176f-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d176f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d176f-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d176f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d176f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d176f-136">CommonParameters</span></span>
<span data-ttu-id="d176f-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d176f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d176f-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d176f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d176f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d176f-139">INPUTS</span></span>

### <span data-ttu-id="d176f-140">Microsoft.Azure.Commands.Security.models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="d176f-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="d176f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d176f-141">System.String</span></span>

## <span data-ttu-id="d176f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d176f-142">OUTPUTS</span></span>

### <span data-ttu-id="d176f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d176f-143">System.Boolean</span></span>

## <span data-ttu-id="d176f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d176f-144">NOTES</span></span>

## <span data-ttu-id="d176f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d176f-145">RELATED LINKS</span></span>
