---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: b2ada8c4a58b38eee9ab235bbcd88429934ac00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902941"
---
# <span data-ttu-id="672d4-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="672d4-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="672d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="672d4-102">SYNOPSIS</span></span>
<span data-ttu-id="672d4-103">在應用程式深入資訊資源中移除連續匯出組</span><span class="sxs-lookup"><span data-stu-id="672d4-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="672d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="672d4-104">SYNTAX</span></span>

### <span data-ttu-id="672d4-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="672d4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="672d4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="672d4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="672d4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="672d4-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672d4-108">描述</span><span class="sxs-lookup"><span data-stu-id="672d4-108">DESCRIPTION</span></span>
<span data-ttu-id="672d4-109">在應用程式深入資訊資源中移除連續匯出組</span><span class="sxs-lookup"><span data-stu-id="672d4-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="672d4-110">例子</span><span class="sxs-lookup"><span data-stu-id="672d4-110">EXAMPLES</span></span>

### <span data-ttu-id="672d4-111">範例 1 移除應用程式深入資訊資源中的連續匯出組</span><span class="sxs-lookup"><span data-stu-id="672d4-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="672d4-112">使用匯出識別碼 "uGOoki0jQsyEs3IdQ83Q4QsNr4=" 移除應用程式深入資訊連續匯出組，以用於資源群組 "testgroup" 中名為 "test" 的資源</span><span class="sxs-lookup"><span data-stu-id="672d4-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="672d4-113">參數</span><span class="sxs-lookup"><span data-stu-id="672d4-113">PARAMETERS</span></span>

### <span data-ttu-id="672d4-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="672d4-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="672d4-115">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="672d4-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="672d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672d4-116">-DefaultProfile</span></span>
<span data-ttu-id="672d4-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="672d4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="672d4-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="672d4-118">-ExportId</span></span>
<span data-ttu-id="672d4-119">應用程式深入資訊連續匯出識別碼。</span><span class="sxs-lookup"><span data-stu-id="672d4-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="672d4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="672d4-120">-Name</span></span>
<span data-ttu-id="672d4-121">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="672d4-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="672d4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="672d4-122">-PassThru</span></span>
<span data-ttu-id="672d4-123">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="672d4-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="672d4-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="672d4-124">This parameter is optional.</span></span> <span data-ttu-id="672d4-125">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="672d4-125">Default value is false.</span></span>

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

### <span data-ttu-id="672d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="672d4-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="672d4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="672d4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="672d4-128">-ResourceId</span></span>
<span data-ttu-id="672d4-129">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="672d4-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="672d4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="672d4-130">-Confirm</span></span>
<span data-ttu-id="672d4-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="672d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672d4-132">-WhatIf</span></span>
<span data-ttu-id="672d4-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="672d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672d4-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="672d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672d4-135">CommonParameters</span></span>
<span data-ttu-id="672d4-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="672d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672d4-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="672d4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672d4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="672d4-138">INPUTS</span></span>

### <span data-ttu-id="672d4-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="672d4-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="672d4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="672d4-140">System.String</span></span>

## <span data-ttu-id="672d4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="672d4-141">OUTPUTS</span></span>

### <span data-ttu-id="672d4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="672d4-142">System.Boolean</span></span>

## <span data-ttu-id="672d4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="672d4-143">NOTES</span></span>

## <span data-ttu-id="672d4-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="672d4-144">RELATED LINKS</span></span>
