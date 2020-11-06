---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 7b47576c0fd506831d8e48201d39bd66fec72032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447508"
---
# <span data-ttu-id="30d2a-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="30d2a-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="30d2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="30d2a-103">針對 application insights 資源設定每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="30d2a-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30d2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="30d2a-104">SYNTAX</span></span>

### <span data-ttu-id="30d2a-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="30d2a-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30d2a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d2a-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d2a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d2a-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30d2a-108">說明</span><span class="sxs-lookup"><span data-stu-id="30d2a-108">DESCRIPTION</span></span>
<span data-ttu-id="30d2a-109">針對 application insights 資源設定每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="30d2a-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="30d2a-110">示例</span><span class="sxs-lookup"><span data-stu-id="30d2a-110">EXAMPLES</span></span>

### <span data-ttu-id="30d2a-111">範例1設定 application insights 資源的每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="30d2a-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="30d2a-112">將 [每日資料 volumen 上限] 設定為 [每日 400GB]，並在 [資源群組 "testgroup 中停止對資源" test "的傳送通知。</span><span class="sxs-lookup"><span data-stu-id="30d2a-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="30d2a-113">參數</span><span class="sxs-lookup"><span data-stu-id="30d2a-113">PARAMETERS</span></span>

### <span data-ttu-id="30d2a-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="30d2a-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="30d2a-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="30d2a-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="30d2a-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="30d2a-116">-DailyCapGB</span></span>
<span data-ttu-id="30d2a-117">每日大寫。</span><span class="sxs-lookup"><span data-stu-id="30d2a-117">Daily Cap.</span></span>

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

### <span data-ttu-id="30d2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d2a-118">-DefaultProfile</span></span>
<span data-ttu-id="30d2a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30d2a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d2a-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="30d2a-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="30d2a-121">當擊中 cap 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="30d2a-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="30d2a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="30d2a-122">-Name</span></span>
<span data-ttu-id="30d2a-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="30d2a-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="30d2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="30d2a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="30d2a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="30d2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30d2a-126">-ResourceId</span></span>
<span data-ttu-id="30d2a-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30d2a-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="30d2a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="30d2a-128">-Confirm</span></span>
<span data-ttu-id="30d2a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30d2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d2a-130">-WhatIf</span></span>
<span data-ttu-id="30d2a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30d2a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30d2a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30d2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d2a-133">CommonParameters</span></span>
<span data-ttu-id="30d2a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30d2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d2a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30d2a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d2a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="30d2a-136">INPUTS</span></span>

### <span data-ttu-id="30d2a-137">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="30d2a-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="30d2a-138">參數： ApplicationInsightsComponent (ByValue) </span><span class="sxs-lookup"><span data-stu-id="30d2a-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="30d2a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="30d2a-139">System.String</span></span>

## <span data-ttu-id="30d2a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="30d2a-140">OUTPUTS</span></span>

### <span data-ttu-id="30d2a-141">PSPricingPlan 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="30d2a-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="30d2a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="30d2a-142">NOTES</span></span>

## <span data-ttu-id="30d2a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="30d2a-143">RELATED LINKS</span></span>
