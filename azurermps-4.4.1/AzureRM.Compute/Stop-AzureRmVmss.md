---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624571"
---
# <span data-ttu-id="c1189-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="c1189-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1189-102">SYNOPSIS</span></span>
<span data-ttu-id="c1189-103">停止 VMSS 中的 VMSS 或一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1189-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1189-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1189-104">SYNTAX</span></span>

### <span data-ttu-id="c1189-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="c1189-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1189-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c1189-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1189-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1189-107">DESCRIPTION</span></span>
<span data-ttu-id="c1189-108">**AzureRmVmss** Cmdlet 會停止虛擬機器規模集中 (VMSS) 或一組虛擬機器中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1189-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c1189-109">您可以使用 *InstanceId* 參數來選取一組虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1189-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c1189-110">示例</span><span class="sxs-lookup"><span data-stu-id="c1189-110">EXAMPLES</span></span>

### <span data-ttu-id="c1189-111">範例1：停止 VMSS 中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c1189-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c1189-112">這個命令會停止屬於名為 ContosoVMSS 之 VMSS 的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1189-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c1189-113">範例2：在 VMSS 中停止一組特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c1189-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="c1189-114">這個命令會停止由屬於名為 ContosoVMSS 之 VMSS 的實例識別碼字串陣列所指定的一組特定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1189-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c1189-115">參數</span><span class="sxs-lookup"><span data-stu-id="c1189-115">PARAMETERS</span></span>

### <span data-ttu-id="c1189-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1189-116">-DefaultProfile</span></span>
<span data-ttu-id="c1189-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1189-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1189-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c1189-118">-Force</span></span>
<span data-ttu-id="c1189-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c1189-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1189-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c1189-120">-InstanceId</span></span>
<span data-ttu-id="c1189-121">指定為字串陣列，此 Cmdlet 停止的虛擬機器實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="c1189-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="c1189-122">舉例來說： `-InstanceId "0", "3"` 。</span><span class="sxs-lookup"><span data-stu-id="c1189-122">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1189-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1189-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1189-124">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1189-124">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1189-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="c1189-125">-StayProvisioned</span></span>
<span data-ttu-id="c1189-126">如果已指定，虛擬機器將會進入 [已停止] 狀態。</span><span class="sxs-lookup"><span data-stu-id="c1189-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="c1189-127">如果未指定，虛擬機器將會輸入已停止解除配置的狀態。</span><span class="sxs-lookup"><span data-stu-id="c1189-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="c1189-128">使用者仍需在已停止狀態的 Vm 中收取費用，但無法在已停止解除配置狀態的 Vm 中使用。</span><span class="sxs-lookup"><span data-stu-id="c1189-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


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

### <span data-ttu-id="c1189-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c1189-129">-VMScaleSetName</span></span>
<span data-ttu-id="c1189-130">指定此 Cmdlet 停止虛擬機器之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1189-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1189-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c1189-131">-Confirm</span></span>
<span data-ttu-id="c1189-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1189-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1189-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1189-133">-WhatIf</span></span>
<span data-ttu-id="c1189-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1189-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1189-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1189-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1189-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1189-136">CommonParameters</span></span>
<span data-ttu-id="c1189-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1189-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1189-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1189-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1189-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c1189-139">INPUTS</span></span>

## <span data-ttu-id="c1189-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c1189-140">OUTPUTS</span></span>

## <span data-ttu-id="c1189-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c1189-141">NOTES</span></span>

## <span data-ttu-id="c1189-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1189-142">RELATED LINKS</span></span>

[<span data-ttu-id="c1189-143">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c1189-144">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c1189-145">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c1189-146">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c1189-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c1189-148">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c1189-149">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c1189-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


