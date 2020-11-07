---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
ms.openlocfilehash: 1c1cdeff1e1a73de6947855922a4fed45fe387e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626135"
---
# <span data-ttu-id="2bbfc-101">Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2bbfc-101">Invoke-AzureRmVmssVMRunCommand</span></span>

## <span data-ttu-id="2bbfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbfc-103">[虛擬機器縮放設定 VM] 上的 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-103">Run command on the Virtual Machine Scale Set VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bbfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bbfc-104">SYNTAX</span></span>

### <span data-ttu-id="2bbfc-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2bbfc-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bbfc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2bbfc-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bbfc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2bbfc-107">ObjectParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bbfc-108">說明</span><span class="sxs-lookup"><span data-stu-id="2bbfc-108">DESCRIPTION</span></span>
<span data-ttu-id="2bbfc-109">在 [虛擬機器縮放設定] VM 上，喚醒呼叫 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2bbfc-110">示例</span><span class="sxs-lookup"><span data-stu-id="2bbfc-110">EXAMPLES</span></span>

### <span data-ttu-id="2bbfc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2bbfc-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2bbfc-112">在資源群組 "rgname" 中，使用「vmssname」的虛擬機器小標集合中的 [sample.ps1] 和 [ID "0 ' VM 中的參數，來喚醒呼叫 RunPowerShellScript 的執行命令。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="2bbfc-113">範例2</span><span class="sxs-lookup"><span data-stu-id="2bbfc-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzureRmVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2bbfc-114">在資源群組 "rgname" 中，使用「vmssname」的虛擬機器小標集合中的 [sample.ps1] 和 [ID "0 ' VM 中的參數，來喚醒呼叫 RunPowerShellScript 的執行命令。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="2bbfc-115">參數</span><span class="sxs-lookup"><span data-stu-id="2bbfc-115">PARAMETERS</span></span>

### <span data-ttu-id="2bbfc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bbfc-116">-AsJob</span></span>
<span data-ttu-id="2bbfc-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2bbfc-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bbfc-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2bbfc-118">-CommandId</span></span>
<span data-ttu-id="2bbfc-119">[執行] 命令 id。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bbfc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbfc-120">-DefaultProfile</span></span>
<span data-ttu-id="2bbfc-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bbfc-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2bbfc-122">-InstanceId</span></span>
<span data-ttu-id="2bbfc-123">虛擬機器縮放集 VM 的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbfc-124">-參數</span><span class="sxs-lookup"><span data-stu-id="2bbfc-124">-Parameter</span></span>
<span data-ttu-id="2bbfc-125">Run 命令參數。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bbfc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bbfc-126">-ResourceGroupName</span></span>
<span data-ttu-id="2bbfc-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2bbfc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bbfc-128">-ResourceId</span></span>
<span data-ttu-id="2bbfc-129">虛擬機器縮放設定 VM 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2bbfc-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="2bbfc-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="2bbfc-130">-ScriptPath</span></span>
<span data-ttu-id="2bbfc-131">要執行之腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-131">Path of the script to be executed.</span></span>  <span data-ttu-id="2bbfc-132">指定此值時，指定的腳本會覆寫命令的預設腳本。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bbfc-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2bbfc-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2bbfc-134">PS 虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbfc-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2bbfc-135">-VMScaleSetName</span></span>
<span data-ttu-id="2bbfc-136">虛擬機器規模設定 VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="2bbfc-137">-確認</span><span class="sxs-lookup"><span data-stu-id="2bbfc-137">-Confirm</span></span>
<span data-ttu-id="2bbfc-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbfc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbfc-139">-WhatIf</span></span>
<span data-ttu-id="2bbfc-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bbfc-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbfc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbfc-142">CommonParameters</span></span>
<span data-ttu-id="2bbfc-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbfc-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbfc-145">輸入</span><span class="sxs-lookup"><span data-stu-id="2bbfc-145">INPUTS</span></span>

### <span data-ttu-id="2bbfc-146">System.object</span><span class="sxs-lookup"><span data-stu-id="2bbfc-146">System.String</span></span>

### <span data-ttu-id="2bbfc-147">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2bbfc-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2bbfc-148">OUTPUTS</span></span>

### <span data-ttu-id="2bbfc-149">PSRunCommandResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2bbfc-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="2bbfc-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2bbfc-150">NOTES</span></span>

## <span data-ttu-id="2bbfc-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bbfc-151">RELATED LINKS</span></span>
