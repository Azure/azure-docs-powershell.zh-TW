---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130138"
---
# <span data-ttu-id="315b5-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="315b5-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="315b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="315b5-102">SYNOPSIS</span></span>
<span data-ttu-id="315b5-103">針對 application insights 資源設定定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="315b5-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="315b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="315b5-104">SYNTAX</span></span>

### <span data-ttu-id="315b5-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="315b5-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="315b5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="315b5-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="315b5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="315b5-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="315b5-108">說明</span><span class="sxs-lookup"><span data-stu-id="315b5-108">DESCRIPTION</span></span>
<span data-ttu-id="315b5-109">針對 application insights 資源設定定價規劃與日常資料量資訊。</span><span class="sxs-lookup"><span data-stu-id="315b5-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="315b5-110">此 Cmdlet 無法設定2018年4月之後所建立的 application insights 定價方案： https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="315b5-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="315b5-111">示例</span><span class="sxs-lookup"><span data-stu-id="315b5-111">EXAMPLES</span></span>

### <span data-ttu-id="315b5-112">範例1設定 application insights 資源的定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="315b5-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="315b5-113">將定價方案設定為 [基本]，將 [每日資料量上限] 設定為 [每日 400GB]，並在 [資源] 群組 "testgroup" 中的資源 "test" 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="315b5-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="315b5-114">參數</span><span class="sxs-lookup"><span data-stu-id="315b5-114">PARAMETERS</span></span>

### <span data-ttu-id="315b5-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="315b5-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="315b5-116">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="315b5-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="315b5-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="315b5-117">-DailyCapGB</span></span>
<span data-ttu-id="315b5-118">每日大寫。</span><span class="sxs-lookup"><span data-stu-id="315b5-118">Daily Cap.</span></span>

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

### <span data-ttu-id="315b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315b5-119">-DefaultProfile</span></span>
<span data-ttu-id="315b5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="315b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315b5-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="315b5-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="315b5-122">當擊中 cap 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="315b5-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="315b5-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="315b5-123">-Name</span></span>
<span data-ttu-id="315b5-124">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="315b5-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="315b5-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="315b5-125">-PricingPlan</span></span>
<span data-ttu-id="315b5-126">定價方案名稱。</span><span class="sxs-lookup"><span data-stu-id="315b5-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="315b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="315b5-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="315b5-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="315b5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="315b5-129">-ResourceId</span></span>
<span data-ttu-id="315b5-130">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="315b5-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="315b5-131">-確認</span><span class="sxs-lookup"><span data-stu-id="315b5-131">-Confirm</span></span>
<span data-ttu-id="315b5-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="315b5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="315b5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="315b5-133">-WhatIf</span></span>
<span data-ttu-id="315b5-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="315b5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="315b5-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="315b5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="315b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315b5-136">CommonParameters</span></span>
<span data-ttu-id="315b5-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="315b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315b5-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="315b5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315b5-139">輸入</span><span class="sxs-lookup"><span data-stu-id="315b5-139">INPUTS</span></span>

### <span data-ttu-id="315b5-140">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="315b5-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="315b5-141">System.object</span><span class="sxs-lookup"><span data-stu-id="315b5-141">System.String</span></span>

## <span data-ttu-id="315b5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="315b5-142">OUTPUTS</span></span>

### <span data-ttu-id="315b5-143">PSPricingPlan 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="315b5-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="315b5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="315b5-144">NOTES</span></span>

## <span data-ttu-id="315b5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="315b5-145">RELATED LINKS</span></span>
