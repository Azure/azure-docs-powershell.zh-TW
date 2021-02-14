---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130139"
---
# <span data-ttu-id="87d78-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="87d78-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="87d78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87d78-102">SYNOPSIS</span></span>
<span data-ttu-id="87d78-103">移除 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="87d78-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="87d78-104">句法</span><span class="sxs-lookup"><span data-stu-id="87d78-104">SYNTAX</span></span>

### <span data-ttu-id="87d78-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="87d78-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d78-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d78-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87d78-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d78-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d78-108">說明</span><span class="sxs-lookup"><span data-stu-id="87d78-108">DESCRIPTION</span></span>
<span data-ttu-id="87d78-109">移除 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="87d78-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="87d78-110">示例</span><span class="sxs-lookup"><span data-stu-id="87d78-110">EXAMPLES</span></span>

### <span data-ttu-id="87d78-111">範例1移除 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="87d78-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="87d78-112">在資源群組 "9C29aa0f867" 中，移除 id 為「dd173f38-4fd1-4c75-8af5-9 testGroup」的特定 application insights api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="87d78-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="87d78-113">參數</span><span class="sxs-lookup"><span data-stu-id="87d78-113">PARAMETERS</span></span>

### <span data-ttu-id="87d78-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="87d78-114">-ApiKeyId</span></span>
<span data-ttu-id="87d78-115">Application Insights API 金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="87d78-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="87d78-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="87d78-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="87d78-117">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="87d78-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="87d78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d78-118">-DefaultProfile</span></span>
<span data-ttu-id="87d78-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87d78-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d78-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="87d78-120">-Name</span></span>
<span data-ttu-id="87d78-121">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="87d78-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="87d78-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87d78-122">-PassThru</span></span>
<span data-ttu-id="87d78-123">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="87d78-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="87d78-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="87d78-124">This parameter is optional.</span></span> <span data-ttu-id="87d78-125">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="87d78-125">Default value is false.</span></span>

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

### <span data-ttu-id="87d78-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d78-126">-ResourceGroupName</span></span>
<span data-ttu-id="87d78-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="87d78-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="87d78-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87d78-128">-ResourceId</span></span>
<span data-ttu-id="87d78-129">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="87d78-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="87d78-130">-確認</span><span class="sxs-lookup"><span data-stu-id="87d78-130">-Confirm</span></span>
<span data-ttu-id="87d78-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87d78-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d78-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d78-132">-WhatIf</span></span>
<span data-ttu-id="87d78-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87d78-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d78-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87d78-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d78-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d78-135">CommonParameters</span></span>
<span data-ttu-id="87d78-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87d78-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d78-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87d78-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d78-138">輸入</span><span class="sxs-lookup"><span data-stu-id="87d78-138">INPUTS</span></span>

### <span data-ttu-id="87d78-139">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="87d78-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="87d78-140">System.object</span><span class="sxs-lookup"><span data-stu-id="87d78-140">System.String</span></span>

## <span data-ttu-id="87d78-141">輸出</span><span class="sxs-lookup"><span data-stu-id="87d78-141">OUTPUTS</span></span>

### <span data-ttu-id="87d78-142">System.object</span><span class="sxs-lookup"><span data-stu-id="87d78-142">System.Boolean</span></span>

## <span data-ttu-id="87d78-143">筆記</span><span class="sxs-lookup"><span data-stu-id="87d78-143">NOTES</span></span>

## <span data-ttu-id="87d78-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="87d78-144">RELATED LINKS</span></span>
