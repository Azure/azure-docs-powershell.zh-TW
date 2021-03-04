---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: ce4c9d8fd297b53eb628ffcc32ad9479e0647dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917505"
---
# <span data-ttu-id="c47fa-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="c47fa-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="c47fa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c47fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c47fa-103">設定應用程式深入資訊資源的每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="c47fa-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="c47fa-104">語法</span><span class="sxs-lookup"><span data-stu-id="c47fa-104">SYNTAX</span></span>

### <span data-ttu-id="c47fa-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c47fa-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c47fa-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c47fa-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c47fa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c47fa-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c47fa-108">描述</span><span class="sxs-lookup"><span data-stu-id="c47fa-108">DESCRIPTION</span></span>
<span data-ttu-id="c47fa-109">設定應用程式深入資訊資源的每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="c47fa-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="c47fa-110">例子</span><span class="sxs-lookup"><span data-stu-id="c47fa-110">EXAMPLES</span></span>

### <span data-ttu-id="c47fa-111">範例 1 設定應用程式深入資訊資源的每日資料量上限</span><span class="sxs-lookup"><span data-stu-id="c47fa-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="c47fa-112">將每日資料量上限設定為每天 400 GB，當資源群組「測試群組」的資源「測試」達到上限時停止傳送通知</span><span class="sxs-lookup"><span data-stu-id="c47fa-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c47fa-113">參數</span><span class="sxs-lookup"><span data-stu-id="c47fa-113">PARAMETERS</span></span>

### <span data-ttu-id="c47fa-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c47fa-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c47fa-115">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="c47fa-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c47fa-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="c47fa-116">-DailyCapGB</span></span>
<span data-ttu-id="c47fa-117">每日上限。</span><span class="sxs-lookup"><span data-stu-id="c47fa-117">Daily Cap.</span></span>

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

### <span data-ttu-id="c47fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c47fa-118">-DefaultProfile</span></span>
<span data-ttu-id="c47fa-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c47fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c47fa-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="c47fa-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="c47fa-121">當達到上限時停止傳送通知。</span><span class="sxs-lookup"><span data-stu-id="c47fa-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="c47fa-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c47fa-122">-Name</span></span>
<span data-ttu-id="c47fa-123">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="c47fa-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c47fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c47fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="c47fa-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c47fa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c47fa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c47fa-126">-ResourceId</span></span>
<span data-ttu-id="c47fa-127">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c47fa-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c47fa-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c47fa-128">-Confirm</span></span>
<span data-ttu-id="c47fa-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c47fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c47fa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c47fa-130">-WhatIf</span></span>
<span data-ttu-id="c47fa-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c47fa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c47fa-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c47fa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c47fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c47fa-133">CommonParameters</span></span>
<span data-ttu-id="c47fa-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c47fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c47fa-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c47fa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c47fa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c47fa-136">INPUTS</span></span>

### <span data-ttu-id="c47fa-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c47fa-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c47fa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c47fa-138">System.String</span></span>

## <span data-ttu-id="c47fa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c47fa-139">OUTPUTS</span></span>

### <span data-ttu-id="c47fa-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c47fa-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="c47fa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c47fa-141">NOTES</span></span>

## <span data-ttu-id="c47fa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c47fa-142">RELATED LINKS</span></span>
