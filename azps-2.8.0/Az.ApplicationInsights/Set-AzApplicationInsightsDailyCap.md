---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: 0283bfcc0c3eecf3ca7f97a8f5bb2b8813c4ae78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613830"
---
# <span data-ttu-id="8ff98-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="8ff98-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="8ff98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ff98-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff98-103">針對 application insights 資源設定每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="8ff98-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="8ff98-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ff98-104">SYNTAX</span></span>

### <span data-ttu-id="8ff98-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8ff98-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ff98-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ff98-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ff98-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ff98-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff98-108">說明</span><span class="sxs-lookup"><span data-stu-id="8ff98-108">DESCRIPTION</span></span>
<span data-ttu-id="8ff98-109">針對 application insights 資源設定每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="8ff98-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="8ff98-110">示例</span><span class="sxs-lookup"><span data-stu-id="8ff98-110">EXAMPLES</span></span>

### <span data-ttu-id="8ff98-111">範例1設定 application insights 資源的每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="8ff98-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="8ff98-112">將 [每日資料量頭] 設定為 [每日 400GB]，並在 [資源] 群組 "testgroup" 中的資源 "test" 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="8ff98-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8ff98-113">參數</span><span class="sxs-lookup"><span data-stu-id="8ff98-113">PARAMETERS</span></span>

### <span data-ttu-id="8ff98-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8ff98-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8ff98-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="8ff98-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8ff98-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="8ff98-116">-DailyCapGB</span></span>
<span data-ttu-id="8ff98-117">每日大寫。</span><span class="sxs-lookup"><span data-stu-id="8ff98-117">Daily Cap.</span></span>

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

### <span data-ttu-id="8ff98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff98-118">-DefaultProfile</span></span>
<span data-ttu-id="8ff98-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ff98-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ff98-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="8ff98-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="8ff98-121">當擊中 cap 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="8ff98-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="8ff98-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ff98-122">-Name</span></span>
<span data-ttu-id="8ff98-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff98-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8ff98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff98-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ff98-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff98-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ff98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ff98-126">-ResourceId</span></span>
<span data-ttu-id="8ff98-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ff98-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8ff98-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8ff98-128">-Confirm</span></span>
<span data-ttu-id="8ff98-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ff98-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ff98-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ff98-130">-WhatIf</span></span>
<span data-ttu-id="8ff98-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ff98-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ff98-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ff98-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ff98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff98-133">CommonParameters</span></span>
<span data-ttu-id="8ff98-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ff98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff98-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ff98-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff98-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8ff98-136">INPUTS</span></span>

### <span data-ttu-id="8ff98-137">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="8ff98-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8ff98-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8ff98-138">System.String</span></span>

## <span data-ttu-id="8ff98-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8ff98-139">OUTPUTS</span></span>

### <span data-ttu-id="8ff98-140">PSPricingPlan 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="8ff98-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="8ff98-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8ff98-141">NOTES</span></span>

## <span data-ttu-id="8ff98-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ff98-142">RELATED LINKS</span></span>
