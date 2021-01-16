---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280763"
---
# <span data-ttu-id="6019c-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="6019c-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="6019c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6019c-102">SYNOPSIS</span></span>
<span data-ttu-id="6019c-103">針對 application insights 資源設定每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="6019c-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="6019c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6019c-104">SYNTAX</span></span>

### <span data-ttu-id="6019c-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6019c-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6019c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6019c-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6019c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6019c-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6019c-108">說明</span><span class="sxs-lookup"><span data-stu-id="6019c-108">DESCRIPTION</span></span>
<span data-ttu-id="6019c-109">針對 application insights 資源設定每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="6019c-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="6019c-110">示例</span><span class="sxs-lookup"><span data-stu-id="6019c-110">EXAMPLES</span></span>

### <span data-ttu-id="6019c-111">範例1設定 application insights 資源的每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="6019c-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="6019c-112">將 [每日資料量頭] 設定為 [每日 400GB]，並在 [資源] 群組 "testgroup" 中的資源 "test" 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="6019c-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="6019c-113">參數</span><span class="sxs-lookup"><span data-stu-id="6019c-113">PARAMETERS</span></span>

### <span data-ttu-id="6019c-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6019c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6019c-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="6019c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6019c-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="6019c-116">-DailyCapGB</span></span>
<span data-ttu-id="6019c-117">每日大寫。</span><span class="sxs-lookup"><span data-stu-id="6019c-117">Daily Cap.</span></span>

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

### <span data-ttu-id="6019c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6019c-118">-DefaultProfile</span></span>
<span data-ttu-id="6019c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6019c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6019c-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="6019c-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="6019c-121">當擊中 cap 時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="6019c-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="6019c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6019c-122">-Name</span></span>
<span data-ttu-id="6019c-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="6019c-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6019c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6019c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6019c-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6019c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6019c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6019c-126">-ResourceId</span></span>
<span data-ttu-id="6019c-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6019c-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6019c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6019c-128">-Confirm</span></span>
<span data-ttu-id="6019c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6019c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6019c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6019c-130">-WhatIf</span></span>
<span data-ttu-id="6019c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6019c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6019c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6019c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6019c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6019c-133">CommonParameters</span></span>
<span data-ttu-id="6019c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6019c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6019c-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6019c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6019c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6019c-136">INPUTS</span></span>

### <span data-ttu-id="6019c-137">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="6019c-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6019c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="6019c-138">System.String</span></span>

## <span data-ttu-id="6019c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6019c-139">OUTPUTS</span></span>

### <span data-ttu-id="6019c-140">PSPricingPlan 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="6019c-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="6019c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6019c-141">NOTES</span></span>

## <span data-ttu-id="6019c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="6019c-142">RELATED LINKS</span></span>
