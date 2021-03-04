---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 152be66a2e1582d9f8377e09e250d3cf044c64db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916774"
---
# <span data-ttu-id="ab6b7-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-101">Stop-AzVmss</span></span>

## <span data-ttu-id="ab6b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6b7-103">在 VMSS 中停止 VMSS 或一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="ab6b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab6b7-104">SYNTAX</span></span>

### <span data-ttu-id="ab6b7-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ab6b7-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab6b7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ab6b7-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab6b7-107">描述</span><span class="sxs-lookup"><span data-stu-id="ab6b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ab6b7-108">**Stop-Az Vmss** Cmdlet 會停止虛擬機器縮放集 (VMSS) 或一組虛擬機器內的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="ab6b7-109">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="ab6b7-110">例子</span><span class="sxs-lookup"><span data-stu-id="ab6b7-110">EXAMPLES</span></span>

### <span data-ttu-id="ab6b7-111">範例 1：停止 VMSS 內的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ab6b7-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ab6b7-112">此命令會停止所有屬於名為 Contoso VMSS 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="ab6b7-113">範例 2：在 VMSS 中停止一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ab6b7-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="ab6b7-114">此命令會停止實例識別碼字串陣列所指定的一組特定虛擬機器，該陣列屬於名為 Contoso VMSS 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="ab6b7-115">參數</span><span class="sxs-lookup"><span data-stu-id="ab6b7-115">PARAMETERS</span></span>

### <span data-ttu-id="ab6b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab6b7-116">-AsJob</span></span>
<span data-ttu-id="ab6b7-117">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ab6b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6b7-118">-DefaultProfile</span></span>
<span data-ttu-id="ab6b7-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab6b7-120">-強制</span><span class="sxs-lookup"><span data-stu-id="ab6b7-120">-Force</span></span>
<span data-ttu-id="ab6b7-121">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab6b7-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ab6b7-122">-InstanceId</span></span>
<span data-ttu-id="ab6b7-123">指定此 Cmdlet 停止的虛擬機器實例識別碼或識別碼，做為字串陣列。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="ab6b7-124">例如 `-InstanceId "0", "3"` ：.</span><span class="sxs-lookup"><span data-stu-id="ab6b7-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="ab6b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab6b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab6b7-126">指定 VMSS 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ab6b7-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="ab6b7-127">-SkipShutdown</span></span>
<span data-ttu-id="ab6b7-128">若要要求非正常關閉 VM</span><span class="sxs-lookup"><span data-stu-id="ab6b7-128">To request non-graceful VM shutdown</span></span>

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

### <span data-ttu-id="ab6b7-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="ab6b7-129">-StayProvisioned</span></span>
<span data-ttu-id="ab6b7-130">如果指定，虛擬機器會進入停止狀態。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="ab6b7-131">如果未指定，虛擬機器會進入已停止處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="ab6b7-132">使用者仍會針對處於停止狀態之虛擬機器收費，但系統不會向已停止處理狀態中的虛擬機器收費。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="ab6b7-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ab6b7-133">-VMScaleSetName</span></span>
<span data-ttu-id="ab6b7-134">指定此 Cmdlet 停止虛擬機器的 VMSS 名稱。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="ab6b7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="ab6b7-135">-Confirm</span></span>
<span data-ttu-id="ab6b7-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab6b7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab6b7-137">-WhatIf</span></span>
<span data-ttu-id="ab6b7-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab6b7-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab6b7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6b7-140">CommonParameters</span></span>
<span data-ttu-id="ab6b7-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab6b7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6b7-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab6b7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6b7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ab6b7-143">INPUTS</span></span>

### <span data-ttu-id="ab6b7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ab6b7-144">System.String</span></span>

### <span data-ttu-id="ab6b7-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ab6b7-145">System.String[]</span></span>

## <span data-ttu-id="ab6b7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ab6b7-146">OUTPUTS</span></span>

### <span data-ttu-id="ab6b7-147">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ab6b7-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ab6b7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ab6b7-148">NOTES</span></span>

## <span data-ttu-id="ab6b7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab6b7-149">RELATED LINKS</span></span>

[<span data-ttu-id="ab6b7-150">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ab6b7-151">New-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ab6b7-152">Remove-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ab6b7-153">Restart-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ab6b7-154">Set-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ab6b7-155">Start-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ab6b7-156">Update-AzEvss</span><span class="sxs-lookup"><span data-stu-id="ab6b7-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


