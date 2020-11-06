---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449930"
---
# <span data-ttu-id="a2e9e-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="a2e9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e9e-103">在指定的 VMSS 上設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2e9e-104">SYNTAX</span></span>

### <span data-ttu-id="a2e9e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="a2e9e-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2e9e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a2e9e-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2e9e-107">說明</span><span class="sxs-lookup"><span data-stu-id="a2e9e-107">DESCRIPTION</span></span>
<span data-ttu-id="a2e9e-108">**AzureRmVmss** Cmdlet 會在虛擬機器縮放集 (VMSS) 設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a2e9e-109">這個 Cmdlet 支援的唯一動作是重新鏡像。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="a2e9e-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2e9e-110">EXAMPLES</span></span>

### <span data-ttu-id="a2e9e-111">範例1：重新鏡像 VMSS</span><span class="sxs-lookup"><span data-stu-id="a2e9e-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a2e9e-112">這個命令會 reimages 名為 ContosoGroup 之資源群組的 VMSS 命名 ContosoVMSS。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="a2e9e-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2e9e-113">PARAMETERS</span></span>

### <span data-ttu-id="a2e9e-114">-重新映射</span><span class="sxs-lookup"><span data-stu-id="a2e9e-114">-Reimage</span></span>
<span data-ttu-id="a2e9e-115">表示 Cmdlet reimages VMSS。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9e-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="a2e9e-116">-ReimageAll</span></span>
<span data-ttu-id="a2e9e-117">表示 Cmdlet reimages VMSS 中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e9e-118">-ResourceGroupName</span></span>
<span data-ttu-id="a2e9e-119">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a2e9e-120">-VMScaleSetName</span></span>
<span data-ttu-id="a2e9e-121">Species 此 Cmdlet 針對其設定動作的 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9e-122">-確認</span><span class="sxs-lookup"><span data-stu-id="a2e9e-122">-Confirm</span></span>
<span data-ttu-id="a2e9e-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e9e-124">-WhatIf</span></span>
<span data-ttu-id="a2e9e-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2e9e-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e9e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e9e-127">CommonParameters</span></span>
<span data-ttu-id="a2e9e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e9e-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e9e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a2e9e-130">INPUTS</span></span>

### <span data-ttu-id="a2e9e-131">所有</span><span class="sxs-lookup"><span data-stu-id="a2e9e-131">None</span></span>
<span data-ttu-id="a2e9e-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2e9e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a2e9e-133">OUTPUTS</span></span>

### <span data-ttu-id="a2e9e-134">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a2e9e-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a2e9e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a2e9e-135">NOTES</span></span>

## <span data-ttu-id="a2e9e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2e9e-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2e9e-137">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a2e9e-138">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a2e9e-139">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a2e9e-140">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a2e9e-141">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a2e9e-142">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a2e9e-143">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2e9e-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


