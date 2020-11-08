---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138216"
---
# <span data-ttu-id="ca139-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-101">Stop-AzVmss</span></span>

## <span data-ttu-id="ca139-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca139-102">SYNOPSIS</span></span>
<span data-ttu-id="ca139-103">停止 VMSS 中的 VMSS 或一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ca139-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="ca139-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca139-104">SYNTAX</span></span>

### <span data-ttu-id="ca139-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ca139-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca139-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ca139-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca139-107">說明</span><span class="sxs-lookup"><span data-stu-id="ca139-107">DESCRIPTION</span></span>
<span data-ttu-id="ca139-108">**AzVmss** Cmdlet 會停止虛擬機器規模集中 (VMSS) 或一組虛擬機器中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ca139-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="ca139-109">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ca139-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="ca139-110">示例</span><span class="sxs-lookup"><span data-stu-id="ca139-110">EXAMPLES</span></span>

### <span data-ttu-id="ca139-111">範例1：停止 VMSS 中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ca139-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ca139-112">這個命令會停止屬於名為 ContosoVMSS 之 VMSS 的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ca139-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="ca139-113">範例2：在 VMSS 中停止一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ca139-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="ca139-114">這個命令會停止由屬於名為 ContosoVMSS 之 VMSS 的實例識別碼字串陣列所指定的一組特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ca139-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="ca139-115">參數</span><span class="sxs-lookup"><span data-stu-id="ca139-115">PARAMETERS</span></span>

### <span data-ttu-id="ca139-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca139-116">-AsJob</span></span>
<span data-ttu-id="ca139-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ca139-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ca139-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca139-118">-DefaultProfile</span></span>
<span data-ttu-id="ca139-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca139-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca139-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ca139-120">-Force</span></span>
<span data-ttu-id="ca139-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ca139-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca139-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ca139-122">-InstanceId</span></span>
<span data-ttu-id="ca139-123">指定為字串陣列，此 Cmdlet 停止的虛擬機器實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="ca139-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="ca139-124">舉例來說： `-InstanceId "0", "3"` 。</span><span class="sxs-lookup"><span data-stu-id="ca139-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca139-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca139-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca139-126">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca139-126">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca139-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="ca139-127">-SkipShutdown</span></span>
<span data-ttu-id="ca139-128">要求不溫和的 VM 關閉</span><span class="sxs-lookup"><span data-stu-id="ca139-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca139-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="ca139-129">-StayProvisioned</span></span>
<span data-ttu-id="ca139-130">如果已指定，虛擬機器將會進入 [已停止] 狀態。</span><span class="sxs-lookup"><span data-stu-id="ca139-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="ca139-131">如果未指定，虛擬機器將會輸入已停止解除配置的狀態。</span><span class="sxs-lookup"><span data-stu-id="ca139-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="ca139-132">使用者仍需在已停止狀態的 Vm 中收取費用，但無法在已停止解除配置狀態的 Vm 中使用。</span><span class="sxs-lookup"><span data-stu-id="ca139-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca139-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ca139-133">-VMScaleSetName</span></span>
<span data-ttu-id="ca139-134">指定此 Cmdlet 停止虛擬機器之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca139-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca139-135">-確認</span><span class="sxs-lookup"><span data-stu-id="ca139-135">-Confirm</span></span>
<span data-ttu-id="ca139-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca139-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca139-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca139-137">-WhatIf</span></span>
<span data-ttu-id="ca139-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca139-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca139-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca139-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca139-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca139-140">CommonParameters</span></span>
<span data-ttu-id="ca139-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca139-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca139-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca139-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca139-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ca139-143">INPUTS</span></span>

### <span data-ttu-id="ca139-144">System.object</span><span class="sxs-lookup"><span data-stu-id="ca139-144">System.String</span></span>

### <span data-ttu-id="ca139-145">System.object []</span><span class="sxs-lookup"><span data-stu-id="ca139-145">System.String[]</span></span>

## <span data-ttu-id="ca139-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ca139-146">OUTPUTS</span></span>

### <span data-ttu-id="ca139-147">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ca139-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ca139-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ca139-148">NOTES</span></span>

## <span data-ttu-id="ca139-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca139-149">RELATED LINKS</span></span>

[<span data-ttu-id="ca139-150">AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ca139-151">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ca139-152">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ca139-153">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ca139-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ca139-155">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ca139-156">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca139-156">Update-AzVmss</span></span>](./Update-AzVmss.md)

