---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: ac5e8bbc65a8435042d9f525cd1a3d35fa050398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917502"
---
# <span data-ttu-id="a6b7f-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a6b7f-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="a6b7f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b7f-103">更新現有的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="a6b7f-103">update an existing application insights resource</span></span>

## <span data-ttu-id="a6b7f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6b7f-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6b7f-105">描述</span><span class="sxs-lookup"><span data-stu-id="a6b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b7f-106">更新現有的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="a6b7f-106">update an existing application insights resource</span></span>

## <span data-ttu-id="a6b7f-107">例子</span><span class="sxs-lookup"><span data-stu-id="a6b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b7f-108">範例 1 更新應用程式深入資訊元件</span><span class="sxs-lookup"><span data-stu-id="a6b7f-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="a6b7f-109">將應用程式深入資訊元件 "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery 兩者更新為「已停用」</span><span class="sxs-lookup"><span data-stu-id="a6b7f-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="a6b7f-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6b7f-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b7f-111">-DefaultProfile</span></span>
<span data-ttu-id="a6b7f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b7f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6b7f-113">-Name</span></span>
<span data-ttu-id="a6b7f-114">應用程式深入資訊資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="a6b7f-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="a6b7f-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="a6b7f-116">存取應用程式深入資訊輸入的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="a6b7f-117">值應為 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="a6b7f-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b7f-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="a6b7f-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="a6b7f-119">存取應用程式深入資訊查詢的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="a6b7f-120">值應為 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="a6b7f-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b7f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b7f-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6b7f-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6b7f-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a6b7f-123">-RetentionInDays</span></span>
<span data-ttu-id="a6b7f-124">保留天數，預設為 90。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b7f-125">-標記</span><span class="sxs-lookup"><span data-stu-id="a6b7f-125">-Tag</span></span>
<span data-ttu-id="a6b7f-126">元件標記。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-126">Component Tags.</span></span>

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

### <span data-ttu-id="a6b7f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a6b7f-127">-Confirm</span></span>
<span data-ttu-id="a6b7f-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b7f-129">-WhatIf</span></span>
<span data-ttu-id="a6b7f-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b7f-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b7f-132">CommonParameters</span></span>
<span data-ttu-id="a6b7f-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6b7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b7f-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6b7f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b7f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a6b7f-135">INPUTS</span></span>

### <span data-ttu-id="a6b7f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a6b7f-136">System.String</span></span>

## <span data-ttu-id="a6b7f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a6b7f-137">OUTPUTS</span></span>

### <span data-ttu-id="a6b7f-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a6b7f-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a6b7f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a6b7f-139">NOTES</span></span>

## <span data-ttu-id="a6b7f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6b7f-140">RELATED LINKS</span></span>
