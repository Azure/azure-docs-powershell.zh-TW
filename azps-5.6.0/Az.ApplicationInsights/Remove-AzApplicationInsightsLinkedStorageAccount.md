---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 377a2b967058de9c0cdae1d4c07ceffc73b1bfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914926"
---
# <span data-ttu-id="9dede-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9dede-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="9dede-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9dede-102">SYNOPSIS</span></span>
<span data-ttu-id="9dede-103">刪除應用程式深入資訊連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="9dede-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="9dede-104">語法</span><span class="sxs-lookup"><span data-stu-id="9dede-104">SYNTAX</span></span>

### <span data-ttu-id="9dede-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9dede-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dede-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dede-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dede-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dede-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dede-108">描述</span><span class="sxs-lookup"><span data-stu-id="9dede-108">DESCRIPTION</span></span>
<span data-ttu-id="9dede-109">刪除應用程式深入資訊連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="9dede-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="9dede-110">例子</span><span class="sxs-lookup"><span data-stu-id="9dede-110">EXAMPLES</span></span>

### <span data-ttu-id="9dede-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9dede-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="9dede-112">刪除與應用程式深入資訊元件 "componentName" 相關聯的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="9dede-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="9dede-113">參數</span><span class="sxs-lookup"><span data-stu-id="9dede-113">PARAMETERS</span></span>

### <span data-ttu-id="9dede-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="9dede-114">-ComponentName</span></span>
<span data-ttu-id="9dede-115">元件名稱</span><span class="sxs-lookup"><span data-stu-id="9dede-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dede-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dede-116">-DefaultProfile</span></span>
<span data-ttu-id="9dede-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dede-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dede-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dede-118">-InputObject</span></span>
<span data-ttu-id="9dede-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9dede-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dede-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dede-120">-ResourceGroupName</span></span>
<span data-ttu-id="9dede-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="9dede-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dede-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dede-122">-ResourceId</span></span>
<span data-ttu-id="9dede-123">元件 ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dede-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dede-124">-確認</span><span class="sxs-lookup"><span data-stu-id="9dede-124">-Confirm</span></span>
<span data-ttu-id="9dede-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9dede-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dede-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dede-126">-WhatIf</span></span>
<span data-ttu-id="9dede-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9dede-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dede-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dede-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dede-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dede-129">CommonParameters</span></span>
<span data-ttu-id="9dede-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9dede-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dede-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dede-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dede-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9dede-132">INPUTS</span></span>

### <span data-ttu-id="9dede-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9dede-133">System.String</span></span>

### <span data-ttu-id="9dede-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9dede-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9dede-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9dede-135">OUTPUTS</span></span>

### <span data-ttu-id="9dede-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9dede-136">System.Boolean</span></span>

## <span data-ttu-id="9dede-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9dede-137">NOTES</span></span>

## <span data-ttu-id="9dede-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dede-138">RELATED LINKS</span></span>
