---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: e0edd9ad095f6f7887e0e3f4951828844d2521c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902918"
---
# <span data-ttu-id="ddf8e-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="ddf8e-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="ddf8e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf8e-103">手動平臺更新網域步進以更新服務結構虛擬機器縮放集的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="ddf8e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddf8e-104">SYNTAX</span></span>

### <span data-ttu-id="ddf8e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ddf8e-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddf8e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ddf8e-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddf8e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ddf8e-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddf8e-108">描述</span><span class="sxs-lookup"><span data-stu-id="ddf8e-108">DESCRIPTION</span></span>
<span data-ttu-id="ddf8e-109">強制手動平臺更新網域步進以更新服務結構虛擬機器縮放集的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="ddf8e-110">例子</span><span class="sxs-lookup"><span data-stu-id="ddf8e-110">EXAMPLES</span></span>

### <span data-ttu-id="ddf8e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ddf8e-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="ddf8e-112">此命令會強制在 UD 0 上針對資源組名和縮放比例集名稱所指定的虛擬機器縮放比例執行服務結構更新。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="ddf8e-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ddf8e-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="ddf8e-114">此命令強制在 UD 1 上針對由 VM 縮放集物件所指定的虛擬機器縮放比例執行服務結構更新。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="ddf8e-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="ddf8e-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="ddf8e-116">此命令強制在 UD 2 上針對資源識別碼所指定的虛擬機器縮放比例執行服務結構更新。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="ddf8e-117">參數</span><span class="sxs-lookup"><span data-stu-id="ddf8e-117">PARAMETERS</span></span>

### <span data-ttu-id="ddf8e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddf8e-118">-AsJob</span></span>
<span data-ttu-id="ddf8e-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddf8e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddf8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf8e-120">-DefaultProfile</span></span>
<span data-ttu-id="ddf8e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf8e-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="ddf8e-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="ddf8e-123">要求手動修復步驟的平臺更新網域。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="ddf8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddf8e-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddf8e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddf8e-126">-ResourceId</span></span>
<span data-ttu-id="ddf8e-127">虛擬機器縮放集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ddf8e-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddf8e-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ddf8e-129">本機虛擬機器縮放集物件</span><span class="sxs-lookup"><span data-stu-id="ddf8e-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="ddf8e-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddf8e-130">-VMScaleSetName</span></span>
<span data-ttu-id="ddf8e-131">虛擬機器縮放集的名稱</span><span class="sxs-lookup"><span data-stu-id="ddf8e-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="ddf8e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ddf8e-132">-Confirm</span></span>
<span data-ttu-id="ddf8e-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf8e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf8e-134">-WhatIf</span></span>
<span data-ttu-id="ddf8e-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddf8e-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf8e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf8e-137">CommonParameters</span></span>
<span data-ttu-id="ddf8e-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddf8e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf8e-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddf8e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf8e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ddf8e-140">INPUTS</span></span>

### <span data-ttu-id="ddf8e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ddf8e-141">System.String</span></span>

### <span data-ttu-id="ddf8e-142">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddf8e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ddf8e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ddf8e-143">OUTPUTS</span></span>

### <span data-ttu-id="ddf8e-144">Microsoft.Azure.Commands.Compute.Automation.models.PSRecovery方程式Response</span><span class="sxs-lookup"><span data-stu-id="ddf8e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="ddf8e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ddf8e-145">NOTES</span></span>

## <span data-ttu-id="ddf8e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddf8e-146">RELATED LINKS</span></span>
