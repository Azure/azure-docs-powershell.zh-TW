---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130158"
---
# <span data-ttu-id="c6f7b-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c6f7b-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="c6f7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f7b-103">建立新的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="c6f7b-103">Create a new application insights resource</span></span>

## <span data-ttu-id="c6f7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6f7b-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f7b-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f7b-106">建立新的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="c6f7b-106">Create a new application insights resource</span></span>

## <span data-ttu-id="c6f7b-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f7b-108">範例1建立新的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="c6f7b-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="c6f7b-109">在資源群組 "testgroup" 中，新增名為「test」的新 application insights 資源，類型為「java」</span><span class="sxs-lookup"><span data-stu-id="c6f7b-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="c6f7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6f7b-110">PARAMETERS</span></span>

### <span data-ttu-id="c6f7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f7b-111">-DefaultProfile</span></span>
<span data-ttu-id="c6f7b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6f7b-113">類型</span><span class="sxs-lookup"><span data-stu-id="c6f7b-113">-Kind</span></span>
<span data-ttu-id="c6f7b-114">應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="c6f7b-115">-Location</span></span>
<span data-ttu-id="c6f7b-116">Application Insights 資源位置。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6f7b-117">-Name</span></span>
<span data-ttu-id="c6f7b-118">Application Insights 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="c6f7b-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="c6f7b-120">存取 Application Insights 攝取的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="c6f7b-121">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="c6f7b-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="c6f7b-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="c6f7b-123">存取 Application Insights 查詢的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="c6f7b-124">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="c6f7b-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f7b-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6f7b-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c6f7b-127">-RetentionInDays</span></span>
<span data-ttu-id="c6f7b-128">保留天數、預設值為90。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6f7b-129">-Tag</span></span>
<span data-ttu-id="c6f7b-130">元件標記。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c6f7b-131">-Confirm</span></span>
<span data-ttu-id="c6f7b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f7b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f7b-133">-WhatIf</span></span>
<span data-ttu-id="c6f7b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6f7b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f7b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f7b-136">CommonParameters</span></span>
<span data-ttu-id="c6f7b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f7b-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f7b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c6f7b-139">INPUTS</span></span>

### <span data-ttu-id="c6f7b-140">所有</span><span class="sxs-lookup"><span data-stu-id="c6f7b-140">None</span></span>

## <span data-ttu-id="c6f7b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c6f7b-141">OUTPUTS</span></span>

### <span data-ttu-id="c6f7b-142">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="c6f7b-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="c6f7b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c6f7b-143">NOTES</span></span>

## <span data-ttu-id="c6f7b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6f7b-144">RELATED LINKS</span></span>
