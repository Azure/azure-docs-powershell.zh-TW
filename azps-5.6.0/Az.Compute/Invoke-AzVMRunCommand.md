---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 8eaf939839a668ea817d8f3529fced76ef71d22e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915598"
---
# <span data-ttu-id="3c9a8-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="3c9a8-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="3c9a8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9a8-103">在 VM 上執行命令。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-103">Run a command on the VM.</span></span>

## <span data-ttu-id="3c9a8-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c9a8-104">SYNTAX</span></span>

### <span data-ttu-id="3c9a8-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="3c9a8-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c9a8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3c9a8-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c9a8-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="3c9a8-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c9a8-108">描述</span><span class="sxs-lookup"><span data-stu-id="3c9a8-108">DESCRIPTION</span></span>
<span data-ttu-id="3c9a8-109">在 VM 上啟動執行命令。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="3c9a8-110">例子</span><span class="sxs-lookup"><span data-stu-id="3c9a8-110">EXAMPLES</span></span>

### <span data-ttu-id="3c9a8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3c9a8-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="3c9a8-112">使用重寫腳本 "sample.ps1" 和資源群組 "rgname" 中 "vmname" VM 上的參數來啟動 RunPowerShellScript 的執行命令。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="3c9a8-113">參數</span><span class="sxs-lookup"><span data-stu-id="3c9a8-113">PARAMETERS</span></span>

### <span data-ttu-id="3c9a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c9a8-114">-AsJob</span></span>
<span data-ttu-id="3c9a8-115">在背景中執行 Cmdlet 並返回工作物件以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="3c9a8-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="3c9a8-116">-CommandId</span></span>
<span data-ttu-id="3c9a8-117">執行命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-117">The run command ID.</span></span>

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

### <span data-ttu-id="3c9a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9a8-118">-DefaultProfile</span></span>
<span data-ttu-id="3c9a8-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c9a8-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="3c9a8-120">-Parameter</span></span>
<span data-ttu-id="3c9a8-121">執行命令參數。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-121">The run command parameters.</span></span>

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

### <span data-ttu-id="3c9a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c9a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="3c9a8-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c9a8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c9a8-124">-ResourceId</span></span>
<span data-ttu-id="3c9a8-125">VM 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="3c9a8-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="3c9a8-126">-ScriptPath</span></span>
<span data-ttu-id="3c9a8-127">要執行之腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-127">Path of the script to be executed.</span></span>  <span data-ttu-id="3c9a8-128">當提供此值時，所給予的腳本會優先于命令的預設腳本。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="3c9a8-129">-VM</span><span class="sxs-lookup"><span data-stu-id="3c9a8-129">-VM</span></span>
<span data-ttu-id="3c9a8-130">PS 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c9a8-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="3c9a8-131">-VMName</span></span>
<span data-ttu-id="3c9a8-132">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="3c9a8-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3c9a8-133">-Confirm</span></span>
<span data-ttu-id="3c9a8-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c9a8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c9a8-135">-WhatIf</span></span>
<span data-ttu-id="3c9a8-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c9a8-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c9a8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9a8-138">CommonParameters</span></span>
<span data-ttu-id="3c9a8-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c9a8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9a8-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c9a8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9a8-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3c9a8-141">INPUTS</span></span>

### <span data-ttu-id="3c9a8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3c9a8-142">System.String</span></span>

### <span data-ttu-id="3c9a8-143">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3c9a8-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3c9a8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3c9a8-144">OUTPUTS</span></span>

### <span data-ttu-id="3c9a8-145">Microsoft.Azure.Commands.Compute.Automation.models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="3c9a8-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="3c9a8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3c9a8-146">NOTES</span></span>

## <span data-ttu-id="3c9a8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c9a8-147">RELATED LINKS</span></span>
