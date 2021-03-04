---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915666"
---
# <span data-ttu-id="72c08-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="72c08-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="72c08-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72c08-102">SYNOPSIS</span></span>
<span data-ttu-id="72c08-103">移除應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="72c08-103">Remove an application insights resource</span></span>

## <span data-ttu-id="72c08-104">語法</span><span class="sxs-lookup"><span data-stu-id="72c08-104">SYNTAX</span></span>

### <span data-ttu-id="72c08-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="72c08-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c08-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72c08-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c08-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72c08-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72c08-108">描述</span><span class="sxs-lookup"><span data-stu-id="72c08-108">DESCRIPTION</span></span>
<span data-ttu-id="72c08-109">移除應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="72c08-109">Remove an application insights resource</span></span>

## <span data-ttu-id="72c08-110">例子</span><span class="sxs-lookup"><span data-stu-id="72c08-110">EXAMPLES</span></span>

### <span data-ttu-id="72c08-111">範例 1 移除應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="72c08-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="72c08-112">在資源群組「測試群組」中移除名為「測試」的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="72c08-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="72c08-113">參數</span><span class="sxs-lookup"><span data-stu-id="72c08-113">PARAMETERS</span></span>

### <span data-ttu-id="72c08-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="72c08-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="72c08-115">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="72c08-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="72c08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c08-116">-DefaultProfile</span></span>
<span data-ttu-id="72c08-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72c08-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72c08-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="72c08-118">-Name</span></span>
<span data-ttu-id="72c08-119">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="72c08-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="72c08-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72c08-120">-PassThru</span></span>
<span data-ttu-id="72c08-121">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="72c08-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="72c08-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="72c08-122">This parameter is optional.</span></span> <span data-ttu-id="72c08-123">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="72c08-123">Default value is false.</span></span>

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

### <span data-ttu-id="72c08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c08-124">-ResourceGroupName</span></span>
<span data-ttu-id="72c08-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="72c08-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="72c08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c08-126">-ResourceId</span></span>
<span data-ttu-id="72c08-127">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="72c08-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="72c08-128">-確認</span><span class="sxs-lookup"><span data-stu-id="72c08-128">-Confirm</span></span>
<span data-ttu-id="72c08-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="72c08-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c08-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72c08-130">-WhatIf</span></span>
<span data-ttu-id="72c08-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72c08-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72c08-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72c08-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c08-133">CommonParameters</span></span>
<span data-ttu-id="72c08-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72c08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c08-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72c08-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c08-136">輸入</span><span class="sxs-lookup"><span data-stu-id="72c08-136">INPUTS</span></span>

### <span data-ttu-id="72c08-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="72c08-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="72c08-138">System.String</span><span class="sxs-lookup"><span data-stu-id="72c08-138">System.String</span></span>

## <span data-ttu-id="72c08-139">輸出</span><span class="sxs-lookup"><span data-stu-id="72c08-139">OUTPUTS</span></span>

### <span data-ttu-id="72c08-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="72c08-140">System.Boolean</span></span>

## <span data-ttu-id="72c08-141">筆記</span><span class="sxs-lookup"><span data-stu-id="72c08-141">NOTES</span></span>

## <span data-ttu-id="72c08-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="72c08-142">RELATED LINKS</span></span>
