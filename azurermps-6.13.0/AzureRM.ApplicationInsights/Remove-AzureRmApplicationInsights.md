---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444099"
---
# <span data-ttu-id="bc98a-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bc98a-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="bc98a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc98a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc98a-103">移除 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="bc98a-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc98a-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc98a-104">SYNTAX</span></span>

### <span data-ttu-id="bc98a-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bc98a-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc98a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc98a-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc98a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc98a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc98a-108">說明</span><span class="sxs-lookup"><span data-stu-id="bc98a-108">DESCRIPTION</span></span>
<span data-ttu-id="bc98a-109">移除 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="bc98a-109">Remove an application insights resource</span></span>

## <span data-ttu-id="bc98a-110">示例</span><span class="sxs-lookup"><span data-stu-id="bc98a-110">EXAMPLES</span></span>

### <span data-ttu-id="bc98a-111">範例1移除 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="bc98a-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="bc98a-112">在資源群組 "testgroup" 中移除名為「test」的 applciation insights 資源</span><span class="sxs-lookup"><span data-stu-id="bc98a-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="bc98a-113">參數</span><span class="sxs-lookup"><span data-stu-id="bc98a-113">PARAMETERS</span></span>

### <span data-ttu-id="bc98a-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bc98a-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="bc98a-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="bc98a-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="bc98a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc98a-116">-DefaultProfile</span></span>
<span data-ttu-id="bc98a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc98a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc98a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc98a-118">-Name</span></span>
<span data-ttu-id="bc98a-119">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="bc98a-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="bc98a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc98a-120">-PassThru</span></span>
<span data-ttu-id="bc98a-121">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="bc98a-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="bc98a-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="bc98a-122">This parameter is optional.</span></span> <span data-ttu-id="bc98a-123">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="bc98a-123">Default value is false.</span></span>

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

### <span data-ttu-id="bc98a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc98a-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc98a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bc98a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="bc98a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc98a-126">-ResourceId</span></span>
<span data-ttu-id="bc98a-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc98a-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="bc98a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="bc98a-128">-Confirm</span></span>
<span data-ttu-id="bc98a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc98a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc98a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc98a-130">-WhatIf</span></span>
<span data-ttu-id="bc98a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc98a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc98a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc98a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc98a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc98a-133">CommonParameters</span></span>
<span data-ttu-id="bc98a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc98a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc98a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc98a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc98a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="bc98a-136">INPUTS</span></span>

### <span data-ttu-id="bc98a-137">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="bc98a-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="bc98a-138">參數： ApplicationInsightsComponent (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bc98a-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="bc98a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bc98a-139">System.String</span></span>

## <span data-ttu-id="bc98a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bc98a-140">OUTPUTS</span></span>

### <span data-ttu-id="bc98a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="bc98a-141">System.Boolean</span></span>

## <span data-ttu-id="bc98a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bc98a-142">NOTES</span></span>

## <span data-ttu-id="bc98a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc98a-143">RELATED LINKS</span></span>
