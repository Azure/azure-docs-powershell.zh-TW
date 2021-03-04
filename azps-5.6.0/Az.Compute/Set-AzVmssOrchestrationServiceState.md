---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: 84f208a18061d7a682fc1662c97811a19590ca65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909858"
---
# <span data-ttu-id="0fb07-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="0fb07-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="0fb07-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0fb07-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb07-103">設定 VMSS 的編集服務狀態。</span><span class="sxs-lookup"><span data-stu-id="0fb07-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="0fb07-104">語法</span><span class="sxs-lookup"><span data-stu-id="0fb07-104">SYNTAX</span></span>

### <span data-ttu-id="0fb07-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="0fb07-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb07-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0fb07-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb07-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0fb07-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb07-108">描述</span><span class="sxs-lookup"><span data-stu-id="0fb07-108">DESCRIPTION</span></span>
<span data-ttu-id="0fb07-109">設定 VMSS 的編集服務狀態。</span><span class="sxs-lookup"><span data-stu-id="0fb07-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="0fb07-110">例子</span><span class="sxs-lookup"><span data-stu-id="0fb07-110">EXAMPLES</span></span>

### <span data-ttu-id="0fb07-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0fb07-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="0fb07-112">此命令會暫停資源群組 "rg" 中 VMSS "vmss1" 上的自動修復服務。</span><span class="sxs-lookup"><span data-stu-id="0fb07-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="0fb07-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="0fb07-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="0fb07-114">此命令在資源群組 "rg" 的 VMSS "vmss1" 上繼續自動修復服務。</span><span class="sxs-lookup"><span data-stu-id="0fb07-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="0fb07-115">參數</span><span class="sxs-lookup"><span data-stu-id="0fb07-115">PARAMETERS</span></span>

### <span data-ttu-id="0fb07-116">-動作</span><span class="sxs-lookup"><span data-stu-id="0fb07-116">-Action</span></span>
<span data-ttu-id="0fb07-117">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="0fb07-117">The action to be performed.</span></span>  <span data-ttu-id="0fb07-118">可能的值為：繼續、暫停。</span><span class="sxs-lookup"><span data-stu-id="0fb07-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb07-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fb07-119">-AsJob</span></span>
<span data-ttu-id="0fb07-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0fb07-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fb07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb07-121">-DefaultProfile</span></span>
<span data-ttu-id="0fb07-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fb07-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fb07-123">-InputObject</span></span>
<span data-ttu-id="0fb07-124">虛擬機器縮放集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="0fb07-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0fb07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb07-125">-ResourceGroupName</span></span>
<span data-ttu-id="0fb07-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fb07-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fb07-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fb07-127">-ResourceId</span></span>
<span data-ttu-id="0fb07-128">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0fb07-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="0fb07-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0fb07-129">-ServiceName</span></span>
<span data-ttu-id="0fb07-130">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fb07-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb07-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0fb07-131">-VMScaleSetName</span></span>
<span data-ttu-id="0fb07-132">虛擬機器縮放集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fb07-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0fb07-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0fb07-133">-Confirm</span></span>
<span data-ttu-id="0fb07-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0fb07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb07-135">-WhatIf</span></span>
<span data-ttu-id="0fb07-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0fb07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fb07-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0fb07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb07-138">CommonParameters</span></span>
<span data-ttu-id="0fb07-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0fb07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb07-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fb07-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb07-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0fb07-141">INPUTS</span></span>

### <span data-ttu-id="0fb07-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0fb07-142">System.String</span></span>

### <span data-ttu-id="0fb07-143">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0fb07-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0fb07-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0fb07-144">OUTPUTS</span></span>

### <span data-ttu-id="0fb07-145">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0fb07-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0fb07-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0fb07-146">NOTES</span></span>

## <span data-ttu-id="0fb07-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fb07-147">RELATED LINKS</span></span>
