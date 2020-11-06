---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454291"
---
# <span data-ttu-id="06e81-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="06e81-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="06e81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06e81-102">SYNOPSIS</span></span>
<span data-ttu-id="06e81-103">針對 application insights 資源設定定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="06e81-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e81-104">句法</span><span class="sxs-lookup"><span data-stu-id="06e81-104">SYNTAX</span></span>

### <span data-ttu-id="06e81-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="06e81-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e81-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e81-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e81-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e81-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06e81-108">說明</span><span class="sxs-lookup"><span data-stu-id="06e81-108">DESCRIPTION</span></span>
<span data-ttu-id="06e81-109">針對 application insights 資源設定定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="06e81-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="06e81-110">示例</span><span class="sxs-lookup"><span data-stu-id="06e81-110">EXAMPLES</span></span>

### <span data-ttu-id="06e81-111">範例1設定 application insights 資源的定價規劃與日常資料量資訊</span><span class="sxs-lookup"><span data-stu-id="06e81-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="06e81-112">將定價方案設定為「基本」，將 [每日資料 volumen 上限] 設定為 [每日]，並在 [資源群組 "中的資源" test "中停止傳送通知 [testgroup]</span><span class="sxs-lookup"><span data-stu-id="06e81-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="06e81-113">參數</span><span class="sxs-lookup"><span data-stu-id="06e81-113">PARAMETERS</span></span>

### <span data-ttu-id="06e81-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="06e81-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="06e81-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="06e81-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-116">-確認</span><span class="sxs-lookup"><span data-stu-id="06e81-116">-Confirm</span></span>
<span data-ttu-id="06e81-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06e81-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="06e81-118">-DailyCapGB</span></span>
<span data-ttu-id="06e81-119">每日大寫。</span><span class="sxs-lookup"><span data-stu-id="06e81-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e81-120">-DefaultProfile</span></span>
<span data-ttu-id="06e81-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06e81-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="06e81-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="06e81-123">當擊中 cap 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="06e81-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="06e81-124">-Name</span></span>
<span data-ttu-id="06e81-125">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="06e81-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="06e81-126">-PricingPlan</span></span>
<span data-ttu-id="06e81-127">定價方案名稱。</span><span class="sxs-lookup"><span data-stu-id="06e81-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e81-128">-ResourceGroupName</span></span>
<span data-ttu-id="06e81-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="06e81-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e81-130">-ResourceId</span></span>
<span data-ttu-id="06e81-131">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="06e81-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e81-132">-WhatIf</span></span>
<span data-ttu-id="06e81-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06e81-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06e81-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06e81-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e81-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e81-135">CommonParameters</span></span>
<span data-ttu-id="06e81-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06e81-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e81-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06e81-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e81-138">輸入</span><span class="sxs-lookup"><span data-stu-id="06e81-138">INPUTS</span></span>

### <span data-ttu-id="06e81-139">System.object</span><span class="sxs-lookup"><span data-stu-id="06e81-139">System.String</span></span>
<span data-ttu-id="06e81-140">"System.object"。</span><span class="sxs-lookup"><span data-stu-id="06e81-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="06e81-141">輸出</span><span class="sxs-lookup"><span data-stu-id="06e81-141">OUTPUTS</span></span>

### <span data-ttu-id="06e81-142">PSPricingTier 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="06e81-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="06e81-143">筆記</span><span class="sxs-lookup"><span data-stu-id="06e81-143">NOTES</span></span>

## <span data-ttu-id="06e81-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="06e81-144">RELATED LINKS</span></span>

