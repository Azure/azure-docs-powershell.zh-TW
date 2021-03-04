---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: ed7114f37cebb093c8ba27ed60c0328234571f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911786"
---
# <span data-ttu-id="6e643-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e643-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="6e643-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e643-102">SYNOPSIS</span></span>
<span data-ttu-id="6e643-103">建立應用程式深入資訊連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="6e643-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="6e643-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e643-104">SYNTAX</span></span>

### <span data-ttu-id="6e643-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6e643-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e643-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e643-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e643-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e643-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e643-108">描述</span><span class="sxs-lookup"><span data-stu-id="6e643-108">DESCRIPTION</span></span>
<span data-ttu-id="6e643-109">建立應用程式深入資訊連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="6e643-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="6e643-110">例子</span><span class="sxs-lookup"><span data-stu-id="6e643-110">EXAMPLES</span></span>

### <span data-ttu-id="6e643-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6e643-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="6e643-112">在元件 "componentName" $account建立連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="6e643-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="6e643-113">參數</span><span class="sxs-lookup"><span data-stu-id="6e643-113">PARAMETERS</span></span>

### <span data-ttu-id="6e643-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="6e643-114">-ComponentName</span></span>
<span data-ttu-id="6e643-115">元件名稱</span><span class="sxs-lookup"><span data-stu-id="6e643-115">Component Name</span></span>

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

### <span data-ttu-id="6e643-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e643-116">-DefaultProfile</span></span>
<span data-ttu-id="6e643-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e643-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e643-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e643-118">-InputObject</span></span>
<span data-ttu-id="6e643-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6e643-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="6e643-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6e643-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="6e643-121">儲存空間帳戶 ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e643-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e643-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e643-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e643-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="6e643-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6e643-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e643-124">-ResourceId</span></span>
<span data-ttu-id="6e643-125">元件 ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e643-125">Component ResourceId</span></span>

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

### <span data-ttu-id="6e643-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6e643-126">-Confirm</span></span>
<span data-ttu-id="6e643-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6e643-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e643-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e643-128">-WhatIf</span></span>
<span data-ttu-id="6e643-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e643-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e643-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e643-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e643-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e643-131">CommonParameters</span></span>
<span data-ttu-id="6e643-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e643-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e643-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e643-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e643-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6e643-134">INPUTS</span></span>

### <span data-ttu-id="6e643-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6e643-135">System.String</span></span>

### <span data-ttu-id="6e643-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6e643-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="6e643-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6e643-137">OUTPUTS</span></span>

### <span data-ttu-id="6e643-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e643-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="6e643-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6e643-139">NOTES</span></span>

## <span data-ttu-id="6e643-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e643-140">RELATED LINKS</span></span>
