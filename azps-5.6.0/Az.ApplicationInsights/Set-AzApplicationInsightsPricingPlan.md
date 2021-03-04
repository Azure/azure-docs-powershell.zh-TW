---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 7f730a59b740b061406f2ba14ccf76fe660aea14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910321"
---
# <span data-ttu-id="eebed-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="eebed-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="eebed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eebed-102">SYNOPSIS</span></span>
<span data-ttu-id="eebed-103">設定應用程式深入資訊資源的價格計畫和每日資料量資訊</span><span class="sxs-lookup"><span data-stu-id="eebed-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="eebed-104">語法</span><span class="sxs-lookup"><span data-stu-id="eebed-104">SYNTAX</span></span>

### <span data-ttu-id="eebed-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eebed-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebed-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebed-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebed-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eebed-108">描述</span><span class="sxs-lookup"><span data-stu-id="eebed-108">DESCRIPTION</span></span>
<span data-ttu-id="eebed-109">設定應用程式深入資訊資源的價格計畫和每日資料量資訊。</span><span class="sxs-lookup"><span data-stu-id="eebed-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="eebed-110">此 Cmdlet 無法設定 2018 年 4 月之後所建立之應用程式深入見解的定價方案： https://docs.microsoft.com/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="eebed-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="eebed-111">例子</span><span class="sxs-lookup"><span data-stu-id="eebed-111">EXAMPLES</span></span>

### <span data-ttu-id="eebed-112">範例 1 設定應用程式深入資訊資源的價格計畫和每日資料量資訊</span><span class="sxs-lookup"><span data-stu-id="eebed-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="eebed-113">將定價方案設定為「基本」、將每日資料量上限設定為每天 400 GB，並停止在資源群組「測試群組」中達到資源「測試」上限時傳送通知</span><span class="sxs-lookup"><span data-stu-id="eebed-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="eebed-114">參數</span><span class="sxs-lookup"><span data-stu-id="eebed-114">PARAMETERS</span></span>

### <span data-ttu-id="eebed-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eebed-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="eebed-116">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="eebed-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eebed-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="eebed-117">-DailyCapGB</span></span>
<span data-ttu-id="eebed-118">每日上限。</span><span class="sxs-lookup"><span data-stu-id="eebed-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebed-119">-DefaultProfile</span></span>
<span data-ttu-id="eebed-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eebed-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eebed-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="eebed-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="eebed-122">當達到上限時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="eebed-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="eebed-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="eebed-123">-Name</span></span>
<span data-ttu-id="eebed-124">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="eebed-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebed-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="eebed-125">-PricingPlan</span></span>
<span data-ttu-id="eebed-126">定價方案名稱。</span><span class="sxs-lookup"><span data-stu-id="eebed-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eebed-127">-ResourceGroupName</span></span>
<span data-ttu-id="eebed-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="eebed-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebed-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eebed-129">-ResourceId</span></span>
<span data-ttu-id="eebed-130">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eebed-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebed-131">-確認</span><span class="sxs-lookup"><span data-stu-id="eebed-131">-Confirm</span></span>
<span data-ttu-id="eebed-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eebed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebed-133">-WhatIf</span></span>
<span data-ttu-id="eebed-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eebed-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eebed-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eebed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebed-136">CommonParameters</span></span>
<span data-ttu-id="eebed-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eebed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebed-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eebed-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebed-139">輸入</span><span class="sxs-lookup"><span data-stu-id="eebed-139">INPUTS</span></span>

### <span data-ttu-id="eebed-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eebed-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="eebed-141">System.String</span><span class="sxs-lookup"><span data-stu-id="eebed-141">System.String</span></span>

## <span data-ttu-id="eebed-142">輸出</span><span class="sxs-lookup"><span data-stu-id="eebed-142">OUTPUTS</span></span>

### <span data-ttu-id="eebed-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="eebed-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="eebed-144">筆記</span><span class="sxs-lookup"><span data-stu-id="eebed-144">NOTES</span></span>

## <span data-ttu-id="eebed-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="eebed-145">RELATED LINKS</span></span>
