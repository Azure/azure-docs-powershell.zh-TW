---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140190"
---
# <span data-ttu-id="c5503-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="c5503-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="c5503-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5503-102">SYNOPSIS</span></span>
<span data-ttu-id="c5503-103">手動平臺更新網域逐步更新在 service fabric 虛擬電腦規模集中更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c5503-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="c5503-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5503-104">SYNTAX</span></span>

### <span data-ttu-id="c5503-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="c5503-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5503-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c5503-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5503-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c5503-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5503-108">說明</span><span class="sxs-lookup"><span data-stu-id="c5503-108">DESCRIPTION</span></span>
<span data-ttu-id="c5503-109">強制執行手動平臺更新網域逐步更新在 service fabric 虛擬電腦規模集中更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c5503-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="c5503-110">示例</span><span class="sxs-lookup"><span data-stu-id="c5503-110">EXAMPLES</span></span>

### <span data-ttu-id="c5503-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c5503-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="c5503-112">這個命令會針對由資源群組名稱和縮放集名稱指定的虛擬機器規模集，強制執行針對 UD 0 的服務結構更新行走。</span><span class="sxs-lookup"><span data-stu-id="c5503-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="c5503-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c5503-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="c5503-114">這個命令會針對由 VM 比例集物件指定的虛擬機器規模集，強制執行針對 UD 1 的服務結構更新行走。</span><span class="sxs-lookup"><span data-stu-id="c5503-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="c5503-115">範例3</span><span class="sxs-lookup"><span data-stu-id="c5503-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="c5503-116">這個命令會針對資源識別碼指定的虛擬電腦規模集，強制執行針對 UD 2 的服務結構更新行走。</span><span class="sxs-lookup"><span data-stu-id="c5503-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="c5503-117">參數</span><span class="sxs-lookup"><span data-stu-id="c5503-117">PARAMETERS</span></span>

### <span data-ttu-id="c5503-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5503-118">-AsJob</span></span>
<span data-ttu-id="c5503-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5503-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5503-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5503-120">-DefaultProfile</span></span>
<span data-ttu-id="c5503-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5503-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5503-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="c5503-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="c5503-123">要求手動恢復審核的平臺更新網域。</span><span class="sxs-lookup"><span data-stu-id="c5503-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5503-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5503-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5503-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5503-126">-ResourceId</span></span>
<span data-ttu-id="c5503-127">虛擬機器規模集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5503-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c5503-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c5503-129">本機虛擬電腦比例集物件</span><span class="sxs-lookup"><span data-stu-id="c5503-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c5503-130">-VMScaleSetName</span></span>
<span data-ttu-id="c5503-131">虛擬機器規模集的名稱</span><span class="sxs-lookup"><span data-stu-id="c5503-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c5503-132">-Confirm</span></span>
<span data-ttu-id="c5503-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c5503-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5503-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5503-134">-WhatIf</span></span>
<span data-ttu-id="c5503-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5503-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5503-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5503-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5503-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5503-137">CommonParameters</span></span>
<span data-ttu-id="c5503-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5503-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5503-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c5503-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5503-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c5503-140">INPUTS</span></span>

### <span data-ttu-id="c5503-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c5503-141">System.String</span></span>

### <span data-ttu-id="c5503-142">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c5503-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c5503-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c5503-143">OUTPUTS</span></span>

### <span data-ttu-id="c5503-144">PSRecoveryWalkResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c5503-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="c5503-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c5503-145">NOTES</span></span>

## <span data-ttu-id="c5503-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5503-146">RELATED LINKS</span></span>
