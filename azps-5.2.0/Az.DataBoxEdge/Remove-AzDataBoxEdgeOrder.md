---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275475"
---
# <span data-ttu-id="8ae2f-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8ae2f-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8ae2f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ae2f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae2f-103">移除裝置的順序。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-103">Removes the order for a device.</span></span>

## <span data-ttu-id="8ae2f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ae2f-104">SYNTAX</span></span>

### <span data-ttu-id="8ae2f-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8ae2f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae2f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ae2f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae2f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ae2f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ae2f-108">說明</span><span class="sxs-lookup"><span data-stu-id="8ae2f-108">DESCRIPTION</span></span>
<span data-ttu-id="8ae2f-109">**AzDataBoxEdgeOrder** Cmdlet 會刪除資料編輯方塊邊緣裝置的現有訂單。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="8ae2f-110">示例</span><span class="sxs-lookup"><span data-stu-id="8ae2f-110">EXAMPLES</span></span>

### <span data-ttu-id="8ae2f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8ae2f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="8ae2f-112">參數</span><span class="sxs-lookup"><span data-stu-id="8ae2f-112">PARAMETERS</span></span>

### <span data-ttu-id="8ae2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae2f-113">-AsJob</span></span>
<span data-ttu-id="8ae2f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ae2f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ae2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae2f-115">-DefaultProfile</span></span>
<span data-ttu-id="8ae2f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ae2f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8ae2f-117">-DeviceName</span></span>
<span data-ttu-id="8ae2f-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="8ae2f-118">Device Name</span></span>

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

### <span data-ttu-id="8ae2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ae2f-119">-InputObject</span></span>
<span data-ttu-id="8ae2f-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="8ae2f-120">Input Object</span></span>

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

### <span data-ttu-id="8ae2f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ae2f-121">-PassThru</span></span>
<span data-ttu-id="8ae2f-122">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="8ae2f-122">returns true if successful</span></span>

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

### <span data-ttu-id="8ae2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ae2f-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8ae2f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8ae2f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ae2f-125">-ResourceId</span></span>
<span data-ttu-id="8ae2f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ae2f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8ae2f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="8ae2f-127">-Confirm</span></span>
<span data-ttu-id="8ae2f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae2f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae2f-129">-WhatIf</span></span>
<span data-ttu-id="8ae2f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ae2f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae2f-132">CommonParameters</span></span>
<span data-ttu-id="8ae2f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae2f-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ae2f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae2f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8ae2f-135">INPUTS</span></span>

### <span data-ttu-id="8ae2f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="8ae2f-136">System.String</span></span>

### <span data-ttu-id="8ae2f-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8ae2f-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8ae2f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8ae2f-138">OUTPUTS</span></span>

### <span data-ttu-id="8ae2f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8ae2f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8ae2f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8ae2f-140">NOTES</span></span>

## <span data-ttu-id="8ae2f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ae2f-141">RELATED LINKS</span></span>
