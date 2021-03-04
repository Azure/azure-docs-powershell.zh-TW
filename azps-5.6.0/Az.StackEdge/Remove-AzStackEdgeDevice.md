---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 174fe29d45d20b1b1e0ed0c3935bfd99ad2e1a87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915750"
---
# <span data-ttu-id="ad065-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ad065-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="ad065-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad065-102">SYNOPSIS</span></span>
<span data-ttu-id="ad065-103">移除 Stack Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="ad065-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="ad065-104">語法</span><span class="sxs-lookup"><span data-stu-id="ad065-104">SYNTAX</span></span>

### <span data-ttu-id="ad065-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ad065-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad065-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad065-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad065-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad065-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad065-108">描述</span><span class="sxs-lookup"><span data-stu-id="ad065-108">DESCRIPTION</span></span>
<span data-ttu-id="ad065-109">**Remove-AzStackEdgeDevice Cmdlet** 會移除 Stack Edge 裝置的配置。</span><span class="sxs-lookup"><span data-stu-id="ad065-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="ad065-110">請注意，只有在您下訂單之後，以及 Microsoft 準備出貨前，才能刪除裝置。</span><span class="sxs-lookup"><span data-stu-id="ad065-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="ad065-111">請參閱有關使用此[Cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)之前刪除資源的檔</span><span class="sxs-lookup"><span data-stu-id="ad065-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="ad065-112">例子</span><span class="sxs-lookup"><span data-stu-id="ad065-112">EXAMPLES</span></span>

### <span data-ttu-id="ad065-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="ad065-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="ad065-114">參數</span><span class="sxs-lookup"><span data-stu-id="ad065-114">PARAMETERS</span></span>

### <span data-ttu-id="ad065-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad065-115">-AsJob</span></span>
<span data-ttu-id="ad065-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad065-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad065-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad065-117">-DefaultProfile</span></span>
<span data-ttu-id="ad065-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad065-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad065-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ad065-119">-DeviceObject</span></span>
<span data-ttu-id="ad065-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="ad065-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad065-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad065-121">-Name</span></span>
<span data-ttu-id="ad065-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ad065-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad065-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad065-123">-PassThru</span></span>
<span data-ttu-id="ad065-124">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="ad065-124">returns true if successful</span></span>

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

### <span data-ttu-id="ad065-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad065-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad065-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="ad065-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ad065-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad065-127">-ResourceId</span></span>
<span data-ttu-id="ad065-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad065-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ad065-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ad065-129">-Confirm</span></span>
<span data-ttu-id="ad065-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ad065-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad065-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad065-131">-WhatIf</span></span>
<span data-ttu-id="ad065-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad065-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad065-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad065-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad065-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad065-134">CommonParameters</span></span>
<span data-ttu-id="ad065-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad065-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad065-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad065-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad065-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ad065-137">INPUTS</span></span>

### <span data-ttu-id="ad065-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ad065-138">System.String</span></span>

### <span data-ttu-id="ad065-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ad065-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ad065-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ad065-140">OUTPUTS</span></span>

### <span data-ttu-id="ad065-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad065-141">System.Boolean</span></span>

## <span data-ttu-id="ad065-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ad065-142">NOTES</span></span>

## <span data-ttu-id="ad065-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad065-143">RELATED LINKS</span></span>
