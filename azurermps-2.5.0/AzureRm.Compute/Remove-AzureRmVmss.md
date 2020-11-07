---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 0d7e14657d22ac8f8431e82b51cee81d62d5328f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801381"
---
# <span data-ttu-id="3ffff-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="3ffff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ffff-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffff-103">移除 VMSS 中的 VMSS 或虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3ffff-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ffff-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ffff-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ffff-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ffff-105">DESCRIPTION</span></span>
<span data-ttu-id="3ffff-106">**AzureRmVmss** Cmdlet 會從 Azure 中移除虛擬電腦縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="3ffff-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="3ffff-107">這個 Cmdlet 也可以用來移除 VMSS 內的特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3ffff-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="3ffff-108">您可以使用 *InstanceId* 參數，在 VMSS 中移除特定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3ffff-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="3ffff-109">示例</span><span class="sxs-lookup"><span data-stu-id="3ffff-109">EXAMPLES</span></span>

### <span data-ttu-id="3ffff-110">範例1：移除 VMSS</span><span class="sxs-lookup"><span data-stu-id="3ffff-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="3ffff-111">這個命令會移除屬於名為 Group001 之資源群組的名為 VMScaleSet001 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="3ffff-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="3ffff-112">範例2：從 VMSS 中移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3ffff-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="3ffff-113">這個命令會從屬於名為 Group002 之資源群組的名稱為 VMSS 的 VMScaleSet002 中，移除範例 ID 為3的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3ffff-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="3ffff-114">參數</span><span class="sxs-lookup"><span data-stu-id="3ffff-114">PARAMETERS</span></span>

### <span data-ttu-id="3ffff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ffff-115">-AsJob</span></span>
<span data-ttu-id="3ffff-116">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3ffff-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffff-117">-DefaultProfile</span></span>
<span data-ttu-id="3ffff-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ffff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffff-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3ffff-119">-Force</span></span>
<span data-ttu-id="3ffff-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3ffff-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffff-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3ffff-121">-InstanceId</span></span>
<span data-ttu-id="3ffff-122">指定為字串陣列，即需要啟動之實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ffff-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="3ffff-123">例如： `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="3ffff-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="3ffff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffff-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ffff-125">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ffff-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="3ffff-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3ffff-126">-VMScaleSetName</span></span>
<span data-ttu-id="3ffff-127">Species 此 Cmdlet 移除之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ffff-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="3ffff-128">如果您指定 *InstanceId* 參數，則 Cmdlet 會從此參數指定的 VMSS 中移除指定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3ffff-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="3ffff-129">-確認</span><span class="sxs-lookup"><span data-stu-id="3ffff-129">-Confirm</span></span>
<span data-ttu-id="3ffff-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ffff-130">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="3ffff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ffff-131">-WhatIf</span></span>
<span data-ttu-id="3ffff-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ffff-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ffff-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ffff-133">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="3ffff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffff-134">CommonParameters</span></span>
<span data-ttu-id="3ffff-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ffff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffff-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ffff-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffff-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3ffff-137">INPUTS</span></span>

### <span data-ttu-id="3ffff-138">所有</span><span class="sxs-lookup"><span data-stu-id="3ffff-138">None</span></span>
<span data-ttu-id="3ffff-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3ffff-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ffff-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3ffff-140">OUTPUTS</span></span>

### <span data-ttu-id="3ffff-141">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3ffff-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3ffff-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3ffff-142">NOTES</span></span>

## <span data-ttu-id="3ffff-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ffff-143">RELATED LINKS</span></span>

[<span data-ttu-id="3ffff-144">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="3ffff-145">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="3ffff-146">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="3ffff-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="3ffff-148">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="3ffff-149">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="3ffff-150">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ffff-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


