---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449932"
---
# <span data-ttu-id="8eeb9-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="8eeb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8eeb9-102">SYNOPSIS</span></span>
<span data-ttu-id="8eeb9-103">移除 VMSS 中的 VMSS 或虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eeb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="8eeb9-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eeb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="8eeb9-105">DESCRIPTION</span></span>
<span data-ttu-id="8eeb9-106">**AzureRmVmss** Cmdlet 會從 Azure 中移除虛擬電腦縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="8eeb9-107">這個 Cmdlet 也可以用來移除 VMSS 內的特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="8eeb9-108">您可以使用 *InstanceId* 參數，在 VMSS 中移除特定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="8eeb9-109">示例</span><span class="sxs-lookup"><span data-stu-id="8eeb9-109">EXAMPLES</span></span>

### <span data-ttu-id="8eeb9-110">範例1：移除 VMSS</span><span class="sxs-lookup"><span data-stu-id="8eeb9-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="8eeb9-111">這個命令會移除屬於名為 Group001 之資源群組的名為 VMScaleSet001 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="8eeb9-112">範例2：從 VMSS 中移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8eeb9-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="8eeb9-113">這個命令會從屬於名為 Group002 之資源群組的名稱為 VMSS 的 VMScaleSet002 中，移除範例 ID 為3的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="8eeb9-114">參數</span><span class="sxs-lookup"><span data-stu-id="8eeb9-114">PARAMETERS</span></span>

### <span data-ttu-id="8eeb9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8eeb9-115">-Force</span></span>
<span data-ttu-id="8eeb9-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eeb9-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8eeb9-117">-InstanceId</span></span>
<span data-ttu-id="8eeb9-118">指定為字串陣列，即需要啟動之實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="8eeb9-119">例如： `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="8eeb9-119">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eeb9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eeb9-120">-ResourceGroupName</span></span>
<span data-ttu-id="8eeb9-121">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="8eeb9-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8eeb9-122">-VMScaleSetName</span></span>
<span data-ttu-id="8eeb9-123">Species 此 Cmdlet 移除之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="8eeb9-124">如果您指定 *InstanceId* 參數，則 Cmdlet 會從此參數指定的 VMSS 中移除指定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="8eeb9-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8eeb9-125">-Confirm</span></span>
<span data-ttu-id="8eeb9-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-126">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="8eeb9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eeb9-127">-WhatIf</span></span>
<span data-ttu-id="8eeb9-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8eeb9-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-129">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="8eeb9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eeb9-130">CommonParameters</span></span>
<span data-ttu-id="8eeb9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eeb9-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eeb9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8eeb9-133">INPUTS</span></span>

### <span data-ttu-id="8eeb9-134">所有</span><span class="sxs-lookup"><span data-stu-id="8eeb9-134">None</span></span>
<span data-ttu-id="8eeb9-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8eeb9-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8eeb9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8eeb9-136">OUTPUTS</span></span>

## <span data-ttu-id="8eeb9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8eeb9-137">NOTES</span></span>

## <span data-ttu-id="8eeb9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8eeb9-138">RELATED LINKS</span></span>

[<span data-ttu-id="8eeb9-139">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="8eeb9-140">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="8eeb9-141">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="8eeb9-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="8eeb9-143">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="8eeb9-144">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="8eeb9-145">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8eeb9-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


