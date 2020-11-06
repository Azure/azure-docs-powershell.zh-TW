---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444659"
---
# <span data-ttu-id="586fa-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="586fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="586fa-102">SYNOPSIS</span></span>
<span data-ttu-id="586fa-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="586fa-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="586fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="586fa-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="586fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="586fa-105">DESCRIPTION</span></span>
<span data-ttu-id="586fa-106">**更新-AzureRmVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="586fa-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="586fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="586fa-107">EXAMPLES</span></span>

### <span data-ttu-id="586fa-108">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="586fa-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="586fa-109">這個命令會將屬於名為 Group001 之資源群組的名稱 VMSS001 的 VMSS 狀態，更新為名為 LocalVMSS 的本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="586fa-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="586fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="586fa-110">PARAMETERS</span></span>

### <span data-ttu-id="586fa-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="586fa-111">-ResourceGroupName</span></span>
<span data-ttu-id="586fa-112">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="586fa-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="586fa-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="586fa-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="586fa-114">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="586fa-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="586fa-115">若要取得 VMSS 物件，請使用 Get-AzureRmVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="586fa-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="586fa-116">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="586fa-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="586fa-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="586fa-117">-VMScaleSetName</span></span>
<span data-ttu-id="586fa-118">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="586fa-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586fa-119">-確認</span><span class="sxs-lookup"><span data-stu-id="586fa-119">-Confirm</span></span>
<span data-ttu-id="586fa-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="586fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="586fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="586fa-121">-WhatIf</span></span>
<span data-ttu-id="586fa-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="586fa-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="586fa-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="586fa-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="586fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586fa-124">CommonParameters</span></span>
<span data-ttu-id="586fa-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="586fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586fa-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="586fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586fa-127">輸入</span><span class="sxs-lookup"><span data-stu-id="586fa-127">INPUTS</span></span>

### <span data-ttu-id="586fa-128">所有</span><span class="sxs-lookup"><span data-stu-id="586fa-128">None</span></span>
<span data-ttu-id="586fa-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="586fa-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="586fa-130">輸出</span><span class="sxs-lookup"><span data-stu-id="586fa-130">OUTPUTS</span></span>

## <span data-ttu-id="586fa-131">筆記</span><span class="sxs-lookup"><span data-stu-id="586fa-131">NOTES</span></span>

## <span data-ttu-id="586fa-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="586fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="586fa-133">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="586fa-134">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="586fa-135">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="586fa-136">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="586fa-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="586fa-138">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="586fa-139">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="586fa-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


