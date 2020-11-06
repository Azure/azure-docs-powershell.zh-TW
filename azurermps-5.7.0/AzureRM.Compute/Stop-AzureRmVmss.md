---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455479"
---
# <span data-ttu-id="b46e7-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="b46e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b46e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b46e7-103">停止 VMSS 中的 VMSS 或一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b46e7-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b46e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b46e7-104">SYNTAX</span></span>

### <span data-ttu-id="b46e7-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b46e7-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b46e7-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b46e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="b46e7-107">DESCRIPTION</span></span>
<span data-ttu-id="b46e7-108">**AzureRmVmss** Cmdlet 會停止虛擬機器規模集中 (VMSS) 或一組虛擬機器中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b46e7-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="b46e7-109">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b46e7-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="b46e7-110">示例</span><span class="sxs-lookup"><span data-stu-id="b46e7-110">EXAMPLES</span></span>

### <span data-ttu-id="b46e7-111">範例1：停止 VMSS 中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b46e7-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b46e7-112">這個命令會停止屬於名為 ContosoVMSS 之 VMSS 的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b46e7-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="b46e7-113">範例2：在 VMSS 中停止一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b46e7-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="b46e7-114">這個命令會停止由屬於名為 ContosoVMSS 之 VMSS 的實例識別碼字串陣列所指定的一組特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b46e7-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b46e7-115">參數</span><span class="sxs-lookup"><span data-stu-id="b46e7-115">PARAMETERS</span></span>

### <span data-ttu-id="b46e7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b46e7-116">-Force</span></span>
<span data-ttu-id="b46e7-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b46e7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b46e7-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b46e7-118">-InstanceId</span></span>
<span data-ttu-id="b46e7-119">指定為字串陣列，此 Cmdlet 停止的虛擬機器實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="b46e7-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="b46e7-120">舉例來說： `-InstanceId "0", "3"` 。</span><span class="sxs-lookup"><span data-stu-id="b46e7-120">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="b46e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b46e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="b46e7-122">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b46e7-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b46e7-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b46e7-123">-StayProvisioned</span></span>
<span data-ttu-id="b46e7-124">如果已指定，虛擬機器將會進入 [已停止] 狀態。</span><span class="sxs-lookup"><span data-stu-id="b46e7-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="b46e7-125">如果未指定，虛擬機器將會輸入已停止解除配置的狀態。</span><span class="sxs-lookup"><span data-stu-id="b46e7-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="b46e7-126">使用者仍需在已停止狀態的 Vm 中收取費用，但無法在已停止解除配置狀態的 Vm 中使用。</span><span class="sxs-lookup"><span data-stu-id="b46e7-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b46e7-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b46e7-127">-VMScaleSetName</span></span>
<span data-ttu-id="b46e7-128">指定此 Cmdlet 停止虛擬機器之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b46e7-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="b46e7-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b46e7-129">-Confirm</span></span>
<span data-ttu-id="b46e7-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b46e7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b46e7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b46e7-131">-WhatIf</span></span>
<span data-ttu-id="b46e7-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b46e7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b46e7-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b46e7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b46e7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46e7-134">CommonParameters</span></span>
<span data-ttu-id="b46e7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b46e7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46e7-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b46e7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46e7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b46e7-137">INPUTS</span></span>

### <span data-ttu-id="b46e7-138">所有</span><span class="sxs-lookup"><span data-stu-id="b46e7-138">None</span></span>
<span data-ttu-id="b46e7-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b46e7-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b46e7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b46e7-140">OUTPUTS</span></span>

## <span data-ttu-id="b46e7-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b46e7-141">NOTES</span></span>

## <span data-ttu-id="b46e7-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b46e7-142">RELATED LINKS</span></span>

[<span data-ttu-id="b46e7-143">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b46e7-144">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b46e7-145">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b46e7-146">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b46e7-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b46e7-148">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b46e7-149">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b46e7-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


