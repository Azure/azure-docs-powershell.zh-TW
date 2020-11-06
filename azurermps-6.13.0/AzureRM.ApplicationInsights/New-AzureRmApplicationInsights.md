---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 48922d3e0cbf8cf322d25657c76ee01e0ee238b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445771"
---
# <span data-ttu-id="98c3b-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="98c3b-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="98c3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="98c3b-103">建立新的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="98c3b-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="98c3b-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98c3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="98c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="98c3b-106">建立新的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="98c3b-106">Create a new application insights resource</span></span>

## <span data-ttu-id="98c3b-107">示例</span><span class="sxs-lookup"><span data-stu-id="98c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="98c3b-108">範例1建立新的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="98c3b-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
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
```

<span data-ttu-id="98c3b-109">在資源群組 "testgroup" 中，新增名為「test」的新 application insights 資源（類型為「java」）。</span><span class="sxs-lookup"><span data-stu-id="98c3b-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="98c3b-110">參數</span><span class="sxs-lookup"><span data-stu-id="98c3b-110">PARAMETERS</span></span>

### <span data-ttu-id="98c3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c3b-111">-DefaultProfile</span></span>
<span data-ttu-id="98c3b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98c3b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c3b-113">類型</span><span class="sxs-lookup"><span data-stu-id="98c3b-113">-Kind</span></span>
<span data-ttu-id="98c3b-114">應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="98c3b-114">Application kind.</span></span>

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

### <span data-ttu-id="98c3b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="98c3b-115">-Location</span></span>
<span data-ttu-id="98c3b-116">Application Insights 資源位置。</span><span class="sxs-lookup"><span data-stu-id="98c3b-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="98c3b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="98c3b-117">-Name</span></span>
<span data-ttu-id="98c3b-118">Application Insights 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="98c3b-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="98c3b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c3b-119">-ResourceGroupName</span></span>
<span data-ttu-id="98c3b-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="98c3b-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="98c3b-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="98c3b-121">-Tag</span></span>
<span data-ttu-id="98c3b-122">元件標記。</span><span class="sxs-lookup"><span data-stu-id="98c3b-122">Component Tags.</span></span>

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

### <span data-ttu-id="98c3b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="98c3b-123">-Confirm</span></span>
<span data-ttu-id="98c3b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98c3b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c3b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c3b-125">-WhatIf</span></span>
<span data-ttu-id="98c3b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98c3b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c3b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98c3b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c3b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c3b-128">CommonParameters</span></span>
<span data-ttu-id="98c3b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98c3b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c3b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98c3b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c3b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="98c3b-131">INPUTS</span></span>

### <span data-ttu-id="98c3b-132">所有</span><span class="sxs-lookup"><span data-stu-id="98c3b-132">None</span></span>

## <span data-ttu-id="98c3b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="98c3b-133">OUTPUTS</span></span>

### <span data-ttu-id="98c3b-134">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="98c3b-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="98c3b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="98c3b-135">NOTES</span></span>

## <span data-ttu-id="98c3b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="98c3b-136">RELATED LINKS</span></span>
