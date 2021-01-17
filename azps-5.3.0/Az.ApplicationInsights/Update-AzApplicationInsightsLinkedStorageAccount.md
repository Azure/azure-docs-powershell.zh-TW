---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287511"
---
# <span data-ttu-id="a3532-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3532-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a3532-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3532-102">SYNOPSIS</span></span>
<span data-ttu-id="a3532-103">更新 application insights 連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a3532-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="a3532-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3532-104">SYNTAX</span></span>

### <span data-ttu-id="a3532-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a3532-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3532-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3532-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3532-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3532-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3532-108">說明</span><span class="sxs-lookup"><span data-stu-id="a3532-108">DESCRIPTION</span></span>
<span data-ttu-id="a3532-109">更新 application insights 連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a3532-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="a3532-110">示例</span><span class="sxs-lookup"><span data-stu-id="a3532-110">EXAMPLES</span></span>

### <span data-ttu-id="a3532-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a3532-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="a3532-112">更新元件 [componentName] 底下的連結儲存空間帳戶，以與 $account 建立關聯</span><span class="sxs-lookup"><span data-stu-id="a3532-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="a3532-113">參數</span><span class="sxs-lookup"><span data-stu-id="a3532-113">PARAMETERS</span></span>

### <span data-ttu-id="a3532-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a3532-114">-ComponentName</span></span>
<span data-ttu-id="a3532-115">元件名稱</span><span class="sxs-lookup"><span data-stu-id="a3532-115">Component Name</span></span>

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

### <span data-ttu-id="a3532-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3532-116">-DefaultProfile</span></span>
<span data-ttu-id="a3532-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3532-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3532-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3532-118">-InputObject</span></span>
<span data-ttu-id="a3532-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a3532-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="a3532-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a3532-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="a3532-121">儲存空間帳戶 ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3532-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="a3532-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3532-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3532-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a3532-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a3532-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3532-124">-ResourceId</span></span>
<span data-ttu-id="a3532-125">元件 ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3532-125">Component ResourceId</span></span>

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

### <span data-ttu-id="a3532-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a3532-126">-Confirm</span></span>
<span data-ttu-id="a3532-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3532-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3532-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3532-128">-WhatIf</span></span>
<span data-ttu-id="a3532-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3532-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3532-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3532-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3532-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3532-131">CommonParameters</span></span>
<span data-ttu-id="a3532-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3532-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3532-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3532-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3532-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a3532-134">INPUTS</span></span>

### <span data-ttu-id="a3532-135">System.object</span><span class="sxs-lookup"><span data-stu-id="a3532-135">System.String</span></span>

### <span data-ttu-id="a3532-136">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="a3532-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a3532-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a3532-137">OUTPUTS</span></span>

### <span data-ttu-id="a3532-138">PSComponentLinkedStorageAccounts 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="a3532-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="a3532-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a3532-139">NOTES</span></span>

## <span data-ttu-id="a3532-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3532-140">RELATED LINKS</span></span>
