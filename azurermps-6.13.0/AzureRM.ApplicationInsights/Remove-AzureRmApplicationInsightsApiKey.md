---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: f850877da71e68f14ec720acb7428e192882efd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444096"
---
# <span data-ttu-id="c6b6f-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c6b6f-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c6b6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b6f-103">移除 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="c6b6f-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6b6f-104">SYNTAX</span></span>

### <span data-ttu-id="c6b6f-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6b6f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6b6f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6b6f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6b6f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6b6f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6b6f-108">說明</span><span class="sxs-lookup"><span data-stu-id="c6b6f-108">DESCRIPTION</span></span>
<span data-ttu-id="c6b6f-109">移除 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="c6b6f-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c6b6f-110">示例</span><span class="sxs-lookup"><span data-stu-id="c6b6f-110">EXAMPLES</span></span>

### <span data-ttu-id="c6b6f-111">範例1移除 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="c6b6f-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="c6b6f-112">在資源群組 "9C29aa0f867" 中，移除 id 為「dd173f38-4fd1-4c75-8af5-9 testGroup」的特定 application insights api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c6b6f-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6b6f-113">PARAMETERS</span></span>

### <span data-ttu-id="c6b6f-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="c6b6f-114">-ApiKeyId</span></span>
<span data-ttu-id="c6b6f-115">Application Insights API 金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="c6b6f-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6b6f-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c6b6f-117">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c6b6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b6f-118">-DefaultProfile</span></span>
<span data-ttu-id="c6b6f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6b6f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6b6f-120">-Name</span></span>
<span data-ttu-id="c6b6f-121">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c6b6f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6b6f-122">-PassThru</span></span>
<span data-ttu-id="c6b6f-123">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c6b6f-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-124">This parameter is optional.</span></span> <span data-ttu-id="c6b6f-125">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-125">Default value is false.</span></span>

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

### <span data-ttu-id="c6b6f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b6f-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6b6f-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6b6f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6b6f-128">-ResourceId</span></span>
<span data-ttu-id="c6b6f-129">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c6b6f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c6b6f-130">-Confirm</span></span>
<span data-ttu-id="c6b6f-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b6f-132">-WhatIf</span></span>
<span data-ttu-id="c6b6f-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b6f-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b6f-135">CommonParameters</span></span>
<span data-ttu-id="c6b6f-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b6f-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b6f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c6b6f-138">INPUTS</span></span>

### <span data-ttu-id="c6b6f-139">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="c6b6f-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="c6b6f-140">參數： ApplicationInsightsComponent (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c6b6f-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="c6b6f-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c6b6f-141">System.String</span></span>

## <span data-ttu-id="c6b6f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c6b6f-142">OUTPUTS</span></span>

### <span data-ttu-id="c6b6f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c6b6f-143">System.Boolean</span></span>

## <span data-ttu-id="c6b6f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c6b6f-144">NOTES</span></span>

## <span data-ttu-id="c6b6f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6b6f-145">RELATED LINKS</span></span>
