---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908593"
---
# <span data-ttu-id="8c556-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8c556-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8c556-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c556-102">SYNOPSIS</span></span>
<span data-ttu-id="8c556-103">設定新的資料方塊 Edge 裝置</span><span class="sxs-lookup"><span data-stu-id="8c556-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="8c556-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c556-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c556-105">描述</span><span class="sxs-lookup"><span data-stu-id="8c556-105">DESCRIPTION</span></span>
<span data-ttu-id="8c556-106">**New-AzDataBoxEdgeDevice Cmdlet** 會設定新的 Data Box Edge 裝置</span><span class="sxs-lookup"><span data-stu-id="8c556-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="8c556-107">例子</span><span class="sxs-lookup"><span data-stu-id="8c556-107">EXAMPLES</span></span>

### <span data-ttu-id="8c556-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8c556-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="8c556-109">參數</span><span class="sxs-lookup"><span data-stu-id="8c556-109">PARAMETERS</span></span>

### <span data-ttu-id="8c556-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c556-110">-AsJob</span></span>
<span data-ttu-id="8c556-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c556-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c556-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c556-112">-DefaultProfile</span></span>
<span data-ttu-id="8c556-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c556-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c556-114">-位置</span><span class="sxs-lookup"><span data-stu-id="8c556-114">-Location</span></span>
<span data-ttu-id="8c556-115">裝置位置</span><span class="sxs-lookup"><span data-stu-id="8c556-115">Location of the device</span></span>

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

### <span data-ttu-id="8c556-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c556-116">-Name</span></span>
<span data-ttu-id="8c556-117">資源名稱</span><span class="sxs-lookup"><span data-stu-id="8c556-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c556-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c556-118">-ResourceGroupName</span></span>
<span data-ttu-id="8c556-119">資源組名</span><span class="sxs-lookup"><span data-stu-id="8c556-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8c556-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="8c556-120">-Sku</span></span>
<span data-ttu-id="8c556-121">可用的 SKU 為 Edge、閘道</span><span class="sxs-lookup"><span data-stu-id="8c556-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="8c556-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8c556-122">-Confirm</span></span>
<span data-ttu-id="8c556-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8c556-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c556-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c556-124">-WhatIf</span></span>
<span data-ttu-id="8c556-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c556-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c556-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c556-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c556-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c556-127">CommonParameters</span></span>
<span data-ttu-id="8c556-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c556-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c556-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c556-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c556-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8c556-130">INPUTS</span></span>

### <span data-ttu-id="8c556-131">沒有</span><span class="sxs-lookup"><span data-stu-id="8c556-131">None</span></span>

## <span data-ttu-id="8c556-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8c556-132">OUTPUTS</span></span>

### <span data-ttu-id="8c556-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8c556-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8c556-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8c556-134">NOTES</span></span>

## <span data-ttu-id="8c556-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c556-135">RELATED LINKS</span></span>
