---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130142"
---
# <span data-ttu-id="e71d1-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e71d1-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="e71d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e71d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e71d1-103">移除 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="e71d1-103">Remove an application insights resource</span></span>

## <span data-ttu-id="e71d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e71d1-104">SYNTAX</span></span>

### <span data-ttu-id="e71d1-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e71d1-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e71d1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e71d1-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e71d1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e71d1-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e71d1-108">說明</span><span class="sxs-lookup"><span data-stu-id="e71d1-108">DESCRIPTION</span></span>
<span data-ttu-id="e71d1-109">移除 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="e71d1-109">Remove an application insights resource</span></span>

## <span data-ttu-id="e71d1-110">示例</span><span class="sxs-lookup"><span data-stu-id="e71d1-110">EXAMPLES</span></span>

### <span data-ttu-id="e71d1-111">範例1移除 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="e71d1-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="e71d1-112">在資源群組 "testgroup" 中移除名為「test」的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="e71d1-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="e71d1-113">參數</span><span class="sxs-lookup"><span data-stu-id="e71d1-113">PARAMETERS</span></span>

### <span data-ttu-id="e71d1-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e71d1-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e71d1-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="e71d1-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="e71d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71d1-116">-DefaultProfile</span></span>
<span data-ttu-id="e71d1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e71d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71d1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e71d1-118">-Name</span></span>
<span data-ttu-id="e71d1-119">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="e71d1-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="e71d1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e71d1-120">-PassThru</span></span>
<span data-ttu-id="e71d1-121">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="e71d1-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="e71d1-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e71d1-122">This parameter is optional.</span></span> <span data-ttu-id="e71d1-123">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="e71d1-123">Default value is false.</span></span>

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

### <span data-ttu-id="e71d1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71d1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e71d1-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e71d1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e71d1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e71d1-126">-ResourceId</span></span>
<span data-ttu-id="e71d1-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e71d1-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e71d1-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e71d1-128">-Confirm</span></span>
<span data-ttu-id="e71d1-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e71d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71d1-130">-WhatIf</span></span>
<span data-ttu-id="e71d1-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e71d1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e71d1-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e71d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71d1-133">CommonParameters</span></span>
<span data-ttu-id="e71d1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e71d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71d1-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e71d1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71d1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e71d1-136">INPUTS</span></span>

### <span data-ttu-id="e71d1-137">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="e71d1-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="e71d1-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e71d1-138">System.String</span></span>

## <span data-ttu-id="e71d1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e71d1-139">OUTPUTS</span></span>

### <span data-ttu-id="e71d1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e71d1-140">System.Boolean</span></span>

## <span data-ttu-id="e71d1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e71d1-141">NOTES</span></span>

## <span data-ttu-id="e71d1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e71d1-142">RELATED LINKS</span></span>
