---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141165"
---
# <span data-ttu-id="759d8-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="759d8-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="759d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="759d8-102">SYNOPSIS</span></span>
<span data-ttu-id="759d8-103">刪除 application insights 連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="759d8-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="759d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="759d8-104">SYNTAX</span></span>

### <span data-ttu-id="759d8-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="759d8-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="759d8-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="759d8-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="759d8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="759d8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="759d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="759d8-108">DESCRIPTION</span></span>
<span data-ttu-id="759d8-109">刪除 application insights 連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="759d8-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="759d8-110">示例</span><span class="sxs-lookup"><span data-stu-id="759d8-110">EXAMPLES</span></span>

### <span data-ttu-id="759d8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="759d8-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="759d8-112">刪除與 application insights 元件 "componentName" 相關聯的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="759d8-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="759d8-113">參數</span><span class="sxs-lookup"><span data-stu-id="759d8-113">PARAMETERS</span></span>

### <span data-ttu-id="759d8-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="759d8-114">-ComponentName</span></span>
<span data-ttu-id="759d8-115">元件名稱</span><span class="sxs-lookup"><span data-stu-id="759d8-115">Component Name</span></span>

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

### <span data-ttu-id="759d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759d8-116">-DefaultProfile</span></span>
<span data-ttu-id="759d8-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="759d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="759d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="759d8-118">-InputObject</span></span>
<span data-ttu-id="759d8-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="759d8-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="759d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="759d8-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="759d8-121">Resource Group Name</span></span>

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

### <span data-ttu-id="759d8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="759d8-122">-ResourceId</span></span>
<span data-ttu-id="759d8-123">元件 ResourceId</span><span class="sxs-lookup"><span data-stu-id="759d8-123">Component ResourceId</span></span>

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

### <span data-ttu-id="759d8-124">-確認</span><span class="sxs-lookup"><span data-stu-id="759d8-124">-Confirm</span></span>
<span data-ttu-id="759d8-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="759d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="759d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="759d8-126">-WhatIf</span></span>
<span data-ttu-id="759d8-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="759d8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="759d8-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="759d8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="759d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759d8-129">CommonParameters</span></span>
<span data-ttu-id="759d8-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="759d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759d8-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="759d8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759d8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="759d8-132">INPUTS</span></span>

### <span data-ttu-id="759d8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="759d8-133">System.String</span></span>

### <span data-ttu-id="759d8-134">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="759d8-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="759d8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="759d8-135">OUTPUTS</span></span>

### <span data-ttu-id="759d8-136">System.object</span><span class="sxs-lookup"><span data-stu-id="759d8-136">System.Boolean</span></span>

## <span data-ttu-id="759d8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="759d8-137">NOTES</span></span>

## <span data-ttu-id="759d8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="759d8-138">RELATED LINKS</span></span>
