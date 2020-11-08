---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128295"
---
# <span data-ttu-id="29349-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="29349-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="29349-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29349-102">SYNOPSIS</span></span>
<span data-ttu-id="29349-103">移除資料編輯方塊邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="29349-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="29349-104">句法</span><span class="sxs-lookup"><span data-stu-id="29349-104">SYNTAX</span></span>

### <span data-ttu-id="29349-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29349-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29349-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29349-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29349-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29349-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29349-108">說明</span><span class="sxs-lookup"><span data-stu-id="29349-108">DESCRIPTION</span></span>
<span data-ttu-id="29349-109">**AzDataBoxEdgeDevice** Cmdlet 會移除資料盒 Edge 裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="29349-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="29349-110">請注意，只有在您下一次訂單之後，才能刪除裝置，且是由 Microsoft 運送準備好。</span><span class="sxs-lookup"><span data-stu-id="29349-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="29349-111">使用這個[Cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)前，請參閱刪除資源的相關檔</span><span class="sxs-lookup"><span data-stu-id="29349-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="29349-112">示例</span><span class="sxs-lookup"><span data-stu-id="29349-112">EXAMPLES</span></span>

### <span data-ttu-id="29349-113">範例1</span><span class="sxs-lookup"><span data-stu-id="29349-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="29349-114">參數</span><span class="sxs-lookup"><span data-stu-id="29349-114">PARAMETERS</span></span>

### <span data-ttu-id="29349-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29349-115">-AsJob</span></span>
<span data-ttu-id="29349-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29349-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29349-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29349-117">-DefaultProfile</span></span>
<span data-ttu-id="29349-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29349-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29349-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29349-119">-InputObject</span></span>
<span data-ttu-id="29349-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="29349-120">Input Object</span></span>

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

### <span data-ttu-id="29349-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="29349-121">-Name</span></span>
<span data-ttu-id="29349-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="29349-122">Resource Name</span></span>

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

### <span data-ttu-id="29349-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29349-123">-PassThru</span></span>
<span data-ttu-id="29349-124">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="29349-124">returns true if successful</span></span>

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

### <span data-ttu-id="29349-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29349-125">-ResourceGroupName</span></span>
<span data-ttu-id="29349-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="29349-126">Resource Group Name</span></span>

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

### <span data-ttu-id="29349-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29349-127">-ResourceId</span></span>
<span data-ttu-id="29349-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="29349-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="29349-129">-確認</span><span class="sxs-lookup"><span data-stu-id="29349-129">-Confirm</span></span>
<span data-ttu-id="29349-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29349-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29349-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29349-131">-WhatIf</span></span>
<span data-ttu-id="29349-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29349-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29349-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29349-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29349-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29349-134">CommonParameters</span></span>
<span data-ttu-id="29349-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29349-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29349-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29349-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29349-137">輸入</span><span class="sxs-lookup"><span data-stu-id="29349-137">INPUTS</span></span>

### <span data-ttu-id="29349-138">System.object</span><span class="sxs-lookup"><span data-stu-id="29349-138">System.String</span></span>

### <span data-ttu-id="29349-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="29349-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="29349-140">輸出</span><span class="sxs-lookup"><span data-stu-id="29349-140">OUTPUTS</span></span>

### <span data-ttu-id="29349-141">System.object</span><span class="sxs-lookup"><span data-stu-id="29349-141">System.Boolean</span></span>

## <span data-ttu-id="29349-142">筆記</span><span class="sxs-lookup"><span data-stu-id="29349-142">NOTES</span></span>

## <span data-ttu-id="29349-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="29349-143">RELATED LINKS</span></span>