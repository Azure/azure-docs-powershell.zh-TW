---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 95f99f629fd32333e06c6194fcaf51837224f4a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902945"
---
# <span data-ttu-id="1aee6-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="1aee6-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="1aee6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1aee6-102">SYNOPSIS</span></span>
<span data-ttu-id="1aee6-103">移除應用程式深入資訊資源的應用程式深入資訊 API 金鑰</span><span class="sxs-lookup"><span data-stu-id="1aee6-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="1aee6-104">語法</span><span class="sxs-lookup"><span data-stu-id="1aee6-104">SYNTAX</span></span>

### <span data-ttu-id="1aee6-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1aee6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aee6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aee6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1aee6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aee6-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aee6-108">描述</span><span class="sxs-lookup"><span data-stu-id="1aee6-108">DESCRIPTION</span></span>
<span data-ttu-id="1aee6-109">移除應用程式深入資訊資源的應用程式深入資訊 API 金鑰</span><span class="sxs-lookup"><span data-stu-id="1aee6-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="1aee6-110">例子</span><span class="sxs-lookup"><span data-stu-id="1aee6-110">EXAMPLES</span></span>

### <span data-ttu-id="1aee6-111">範例 1 移除應用程式深入資訊資源的應用程式深入資訊 api 金鑰</span><span class="sxs-lookup"><span data-stu-id="1aee6-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="1aee6-112">移除識別碼為 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" 的特定應用程式深入資訊 api 金鑰，以在資源群組 "testGroup" 中"測試"資源。</span><span class="sxs-lookup"><span data-stu-id="1aee6-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="1aee6-113">參數</span><span class="sxs-lookup"><span data-stu-id="1aee6-113">PARAMETERS</span></span>

### <span data-ttu-id="1aee6-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="1aee6-114">-ApiKeyId</span></span>
<span data-ttu-id="1aee6-115">應用程式深入資訊 API 金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="1aee6-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="1aee6-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1aee6-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="1aee6-117">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="1aee6-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="1aee6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aee6-118">-DefaultProfile</span></span>
<span data-ttu-id="1aee6-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1aee6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aee6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1aee6-120">-Name</span></span>
<span data-ttu-id="1aee6-121">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="1aee6-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="1aee6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aee6-122">-PassThru</span></span>
<span data-ttu-id="1aee6-123">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="1aee6-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="1aee6-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="1aee6-124">This parameter is optional.</span></span> <span data-ttu-id="1aee6-125">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="1aee6-125">Default value is false.</span></span>

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

### <span data-ttu-id="1aee6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aee6-126">-ResourceGroupName</span></span>
<span data-ttu-id="1aee6-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1aee6-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="1aee6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aee6-128">-ResourceId</span></span>
<span data-ttu-id="1aee6-129">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1aee6-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="1aee6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1aee6-130">-Confirm</span></span>
<span data-ttu-id="1aee6-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1aee6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aee6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aee6-132">-WhatIf</span></span>
<span data-ttu-id="1aee6-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1aee6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aee6-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1aee6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aee6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aee6-135">CommonParameters</span></span>
<span data-ttu-id="1aee6-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1aee6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aee6-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1aee6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aee6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1aee6-138">INPUTS</span></span>

### <span data-ttu-id="1aee6-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1aee6-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="1aee6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1aee6-140">System.String</span></span>

## <span data-ttu-id="1aee6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1aee6-141">OUTPUTS</span></span>

### <span data-ttu-id="1aee6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1aee6-142">System.Boolean</span></span>

## <span data-ttu-id="1aee6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1aee6-143">NOTES</span></span>

## <span data-ttu-id="1aee6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1aee6-144">RELATED LINKS</span></span>
