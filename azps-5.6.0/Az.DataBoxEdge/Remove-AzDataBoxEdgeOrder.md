---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 8fe4787ca14d26b7e734a0ac081cdbaef8eddbd9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916982"
---
# <span data-ttu-id="58ec0-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="58ec0-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="58ec0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="58ec0-103">移除裝置的順序。</span><span class="sxs-lookup"><span data-stu-id="58ec0-103">Removes the order for a device.</span></span>

## <span data-ttu-id="58ec0-104">語法</span><span class="sxs-lookup"><span data-stu-id="58ec0-104">SYNTAX</span></span>

### <span data-ttu-id="58ec0-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58ec0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ec0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58ec0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ec0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58ec0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ec0-108">描述</span><span class="sxs-lookup"><span data-stu-id="58ec0-108">DESCRIPTION</span></span>
<span data-ttu-id="58ec0-109">**Remove-AzDataBoxEdgeOrder** Cmdlet 會刪除 Data Box Edge 裝置的現有訂單。</span><span class="sxs-lookup"><span data-stu-id="58ec0-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="58ec0-110">例子</span><span class="sxs-lookup"><span data-stu-id="58ec0-110">EXAMPLES</span></span>

### <span data-ttu-id="58ec0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="58ec0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="58ec0-112">參數</span><span class="sxs-lookup"><span data-stu-id="58ec0-112">PARAMETERS</span></span>

### <span data-ttu-id="58ec0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58ec0-113">-AsJob</span></span>
<span data-ttu-id="58ec0-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58ec0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58ec0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ec0-115">-DefaultProfile</span></span>
<span data-ttu-id="58ec0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58ec0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58ec0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="58ec0-117">-DeviceName</span></span>
<span data-ttu-id="58ec0-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="58ec0-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ec0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58ec0-119">-InputObject</span></span>
<span data-ttu-id="58ec0-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="58ec0-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58ec0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58ec0-121">-PassThru</span></span>
<span data-ttu-id="58ec0-122">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="58ec0-122">returns true if successful</span></span>

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

### <span data-ttu-id="58ec0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ec0-123">-ResourceGroupName</span></span>
<span data-ttu-id="58ec0-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="58ec0-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ec0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ec0-125">-ResourceId</span></span>
<span data-ttu-id="58ec0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ec0-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ec0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="58ec0-127">-Confirm</span></span>
<span data-ttu-id="58ec0-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58ec0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ec0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ec0-129">-WhatIf</span></span>
<span data-ttu-id="58ec0-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58ec0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58ec0-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58ec0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ec0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ec0-132">CommonParameters</span></span>
<span data-ttu-id="58ec0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58ec0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ec0-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58ec0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ec0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="58ec0-135">INPUTS</span></span>

### <span data-ttu-id="58ec0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="58ec0-136">System.String</span></span>

### <span data-ttu-id="58ec0-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="58ec0-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="58ec0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="58ec0-138">OUTPUTS</span></span>

### <span data-ttu-id="58ec0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="58ec0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="58ec0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="58ec0-140">NOTES</span></span>

## <span data-ttu-id="58ec0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="58ec0-141">RELATED LINKS</span></span>
