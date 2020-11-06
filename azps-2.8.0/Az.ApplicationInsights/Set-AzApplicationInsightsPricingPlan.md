---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 13bd076488e8bb379e3b365c6c4d7803ea650f40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613828"
---
# <span data-ttu-id="efbba-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="efbba-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="efbba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efbba-102">SYNOPSIS</span></span>
<span data-ttu-id="efbba-103">針對 application insights 資源設定定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="efbba-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="efbba-104">句法</span><span class="sxs-lookup"><span data-stu-id="efbba-104">SYNTAX</span></span>

### <span data-ttu-id="efbba-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="efbba-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efbba-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efbba-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efbba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efbba-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efbba-108">說明</span><span class="sxs-lookup"><span data-stu-id="efbba-108">DESCRIPTION</span></span>
<span data-ttu-id="efbba-109">針對 application insights 資源設定定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="efbba-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="efbba-110">示例</span><span class="sxs-lookup"><span data-stu-id="efbba-110">EXAMPLES</span></span>

### <span data-ttu-id="efbba-111">範例1設定 application insights 資源的定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="efbba-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="efbba-112">將定價方案設定為 [基本]，將 [每日資料量上限] 設定為 [每日 400GB]，並在 [資源] 群組 "testgroup" 中的資源 "test" 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="efbba-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="efbba-113">參數</span><span class="sxs-lookup"><span data-stu-id="efbba-113">PARAMETERS</span></span>

### <span data-ttu-id="efbba-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="efbba-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="efbba-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="efbba-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="efbba-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="efbba-116">-DailyCapGB</span></span>
<span data-ttu-id="efbba-117">每日大寫。</span><span class="sxs-lookup"><span data-stu-id="efbba-117">Daily Cap.</span></span>

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

### <span data-ttu-id="efbba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbba-118">-DefaultProfile</span></span>
<span data-ttu-id="efbba-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efbba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efbba-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="efbba-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="efbba-121">當擊中 cap 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="efbba-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="efbba-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="efbba-122">-Name</span></span>
<span data-ttu-id="efbba-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="efbba-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="efbba-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="efbba-124">-PricingPlan</span></span>
<span data-ttu-id="efbba-125">定價方案名稱。</span><span class="sxs-lookup"><span data-stu-id="efbba-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="efbba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efbba-126">-ResourceGroupName</span></span>
<span data-ttu-id="efbba-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="efbba-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="efbba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efbba-128">-ResourceId</span></span>
<span data-ttu-id="efbba-129">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="efbba-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="efbba-130">-確認</span><span class="sxs-lookup"><span data-stu-id="efbba-130">-Confirm</span></span>
<span data-ttu-id="efbba-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efbba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efbba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efbba-132">-WhatIf</span></span>
<span data-ttu-id="efbba-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efbba-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efbba-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efbba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efbba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbba-135">CommonParameters</span></span>
<span data-ttu-id="efbba-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efbba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbba-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efbba-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbba-138">輸入</span><span class="sxs-lookup"><span data-stu-id="efbba-138">INPUTS</span></span>

### <span data-ttu-id="efbba-139">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="efbba-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="efbba-140">System.object</span><span class="sxs-lookup"><span data-stu-id="efbba-140">System.String</span></span>

## <span data-ttu-id="efbba-141">輸出</span><span class="sxs-lookup"><span data-stu-id="efbba-141">OUTPUTS</span></span>

### <span data-ttu-id="efbba-142">PSPricingPlan 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="efbba-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="efbba-143">筆記</span><span class="sxs-lookup"><span data-stu-id="efbba-143">NOTES</span></span>

## <span data-ttu-id="efbba-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="efbba-144">RELATED LINKS</span></span>
