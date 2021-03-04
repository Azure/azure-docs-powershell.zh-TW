---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1f2c2e2bf02718053d3656b084f845f40215aceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911138"
---
# <span data-ttu-id="ccb64-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ccb64-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ccb64-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ccb64-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb64-103">移除資料方塊 Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="ccb64-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="ccb64-104">語法</span><span class="sxs-lookup"><span data-stu-id="ccb64-104">SYNTAX</span></span>

### <span data-ttu-id="ccb64-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ccb64-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb64-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccb64-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb64-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccb64-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb64-108">描述</span><span class="sxs-lookup"><span data-stu-id="ccb64-108">DESCRIPTION</span></span>
<span data-ttu-id="ccb64-109">**Remove-AzDataBoxEdgeDevice Cmdlet** 會移除 Data Box Edge 裝置的配置。</span><span class="sxs-lookup"><span data-stu-id="ccb64-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="ccb64-110">請注意，只有在您下訂單之後，以及 Microsoft 準備出貨前，才能刪除裝置。</span><span class="sxs-lookup"><span data-stu-id="ccb64-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="ccb64-111">請參閱有關使用此[Cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)之前刪除資源的檔</span><span class="sxs-lookup"><span data-stu-id="ccb64-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="ccb64-112">例子</span><span class="sxs-lookup"><span data-stu-id="ccb64-112">EXAMPLES</span></span>

### <span data-ttu-id="ccb64-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="ccb64-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="ccb64-114">參數</span><span class="sxs-lookup"><span data-stu-id="ccb64-114">PARAMETERS</span></span>

### <span data-ttu-id="ccb64-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccb64-115">-AsJob</span></span>
<span data-ttu-id="ccb64-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ccb64-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccb64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb64-117">-DefaultProfile</span></span>
<span data-ttu-id="ccb64-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccb64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccb64-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccb64-119">-InputObject</span></span>
<span data-ttu-id="ccb64-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="ccb64-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb64-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ccb64-121">-Name</span></span>
<span data-ttu-id="ccb64-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ccb64-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb64-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccb64-123">-PassThru</span></span>
<span data-ttu-id="ccb64-124">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="ccb64-124">returns true if successful</span></span>

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

### <span data-ttu-id="ccb64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb64-125">-ResourceGroupName</span></span>
<span data-ttu-id="ccb64-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="ccb64-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb64-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccb64-127">-ResourceId</span></span>
<span data-ttu-id="ccb64-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccb64-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ccb64-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ccb64-129">-Confirm</span></span>
<span data-ttu-id="ccb64-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ccb64-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb64-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb64-131">-WhatIf</span></span>
<span data-ttu-id="ccb64-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccb64-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccb64-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccb64-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb64-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb64-134">CommonParameters</span></span>
<span data-ttu-id="ccb64-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ccb64-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb64-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccb64-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb64-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ccb64-137">INPUTS</span></span>

### <span data-ttu-id="ccb64-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ccb64-138">System.String</span></span>

### <span data-ttu-id="ccb64-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ccb64-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ccb64-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ccb64-140">OUTPUTS</span></span>

### <span data-ttu-id="ccb64-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ccb64-141">System.Boolean</span></span>

## <span data-ttu-id="ccb64-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ccb64-142">NOTES</span></span>

## <span data-ttu-id="ccb64-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccb64-143">RELATED LINKS</span></span>
