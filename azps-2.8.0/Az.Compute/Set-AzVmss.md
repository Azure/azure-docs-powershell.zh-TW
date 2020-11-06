---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: ce71ad0e82e7082c199d4823c3a3a59be972ec60
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613138"
---
# <span data-ttu-id="1eef9-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-101">Set-AzVmss</span></span>

## <span data-ttu-id="1eef9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1eef9-102">SYNOPSIS</span></span>
<span data-ttu-id="1eef9-103">在指定的 VMSS 上設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="1eef9-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="1eef9-104">句法</span><span class="sxs-lookup"><span data-stu-id="1eef9-104">SYNTAX</span></span>

### <span data-ttu-id="1eef9-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="1eef9-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eef9-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="1eef9-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eef9-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="1eef9-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eef9-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="1eef9-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1eef9-109">說明</span><span class="sxs-lookup"><span data-stu-id="1eef9-109">DESCRIPTION</span></span>
<span data-ttu-id="1eef9-110">**AzVmss** Cmdlet 會在虛擬機器縮放集 (VMSS) 設定特定動作。</span><span class="sxs-lookup"><span data-stu-id="1eef9-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="1eef9-111">這個 Cmdlet 支援的唯一動作是重新鏡像。</span><span class="sxs-lookup"><span data-stu-id="1eef9-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="1eef9-112">示例</span><span class="sxs-lookup"><span data-stu-id="1eef9-112">EXAMPLES</span></span>

### <span data-ttu-id="1eef9-113">範例1：重新鏡像 VMSS</span><span class="sxs-lookup"><span data-stu-id="1eef9-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="1eef9-114">這個命令會 reimages 名為 ContosoGroup 之資源群組的 VMSS 命名 ContosoVMSS。</span><span class="sxs-lookup"><span data-stu-id="1eef9-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="1eef9-115">參數</span><span class="sxs-lookup"><span data-stu-id="1eef9-115">PARAMETERS</span></span>

### <span data-ttu-id="1eef9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eef9-116">-AsJob</span></span>
<span data-ttu-id="1eef9-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="1eef9-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1eef9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eef9-118">-DefaultProfile</span></span>
<span data-ttu-id="1eef9-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1eef9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eef9-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1eef9-120">-InstanceId</span></span>
<span data-ttu-id="1eef9-121">虛擬機器的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="1eef9-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1eef9-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="1eef9-122">-PerformMaintenance</span></span>
<span data-ttu-id="1eef9-123">表示此 Cmdlet 會在 VMSS 中執行一或多個虛擬機器的維護作業。</span><span class="sxs-lookup"><span data-stu-id="1eef9-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eef9-124">-重新部署</span><span class="sxs-lookup"><span data-stu-id="1eef9-124">-Redeploy</span></span>
<span data-ttu-id="1eef9-125">表示 Cmdlet redeploys VMSS 中的一或多個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1eef9-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eef9-126">-重新映射</span><span class="sxs-lookup"><span data-stu-id="1eef9-126">-Reimage</span></span>
<span data-ttu-id="1eef9-127">表示 Cmdlet reimages VMSS。</span><span class="sxs-lookup"><span data-stu-id="1eef9-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eef9-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="1eef9-128">-ReimageAll</span></span>
<span data-ttu-id="1eef9-129">表示 Cmdlet reimages VMSS 中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="1eef9-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="1eef9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eef9-130">-ResourceGroupName</span></span>
<span data-ttu-id="1eef9-131">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eef9-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="1eef9-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="1eef9-132">-TempDisk</span></span>
<span data-ttu-id="1eef9-133">指定是否要重新鏡像 temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="1eef9-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eef9-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1eef9-134">-VMScaleSetName</span></span>
<span data-ttu-id="1eef9-135">Species 此 Cmdlet 針對其設定動作的 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eef9-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="1eef9-136">-確認</span><span class="sxs-lookup"><span data-stu-id="1eef9-136">-Confirm</span></span>
<span data-ttu-id="1eef9-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1eef9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eef9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eef9-138">-WhatIf</span></span>
<span data-ttu-id="1eef9-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1eef9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1eef9-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1eef9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eef9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eef9-141">CommonParameters</span></span>
<span data-ttu-id="1eef9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1eef9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eef9-143">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1eef9-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eef9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="1eef9-144">INPUTS</span></span>

### <span data-ttu-id="1eef9-145">System.object</span><span class="sxs-lookup"><span data-stu-id="1eef9-145">System.String</span></span>

### <span data-ttu-id="1eef9-146">System.object []</span><span class="sxs-lookup"><span data-stu-id="1eef9-146">System.String[]</span></span>

## <span data-ttu-id="1eef9-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1eef9-147">OUTPUTS</span></span>

### <span data-ttu-id="1eef9-148">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1eef9-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1eef9-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1eef9-149">NOTES</span></span>

## <span data-ttu-id="1eef9-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1eef9-150">RELATED LINKS</span></span>

[<span data-ttu-id="1eef9-151">AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="1eef9-152">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="1eef9-153">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="1eef9-154">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="1eef9-155">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="1eef9-156">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="1eef9-157">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1eef9-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


