---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625918"
---
# <span data-ttu-id="339e5-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="339e5-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="339e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="339e5-102">SYNOPSIS</span></span>
<span data-ttu-id="339e5-103">在 VM 上執行命令。</span><span class="sxs-lookup"><span data-stu-id="339e5-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="339e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="339e5-104">SYNTAX</span></span>

### <span data-ttu-id="339e5-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="339e5-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339e5-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="339e5-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="339e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="339e5-107">DESCRIPTION</span></span>
<span data-ttu-id="339e5-108">在 VM 上喚醒 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="339e5-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="339e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="339e5-109">EXAMPLES</span></span>

### <span data-ttu-id="339e5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="339e5-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="339e5-111">在資源群組 [rgname] 中，sample.ps1 使用 [vmname] 的 VM 中的 [RunPowerShellScript] 和 [VM] 中的參數，來喚醒呼叫 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="339e5-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="339e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="339e5-112">PARAMETERS</span></span>

### <span data-ttu-id="339e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="339e5-113">-AsJob</span></span>
<span data-ttu-id="339e5-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="339e5-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="339e5-115">-CommandId</span></span>
<span data-ttu-id="339e5-116">[執行] 命令 id。</span><span class="sxs-lookup"><span data-stu-id="339e5-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339e5-117">-DefaultProfile</span></span>
<span data-ttu-id="339e5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="339e5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-119">-參數</span><span class="sxs-lookup"><span data-stu-id="339e5-119">-Parameter</span></span>
<span data-ttu-id="339e5-120">Run 命令參數。</span><span class="sxs-lookup"><span data-stu-id="339e5-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="339e5-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="339e5-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="339e5-123">-ScriptPath</span></span>
<span data-ttu-id="339e5-124">要執行之腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="339e5-124">Path of the script to be executed.</span></span>  <span data-ttu-id="339e5-125">指定此值時，指定的腳本會覆寫命令的預設腳本。</span><span class="sxs-lookup"><span data-stu-id="339e5-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-126">-VM</span><span class="sxs-lookup"><span data-stu-id="339e5-126">-VM</span></span>
<span data-ttu-id="339e5-127">PS 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="339e5-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="339e5-128">-VMName</span></span>
<span data-ttu-id="339e5-129">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="339e5-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="339e5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="339e5-130">-Confirm</span></span>
<span data-ttu-id="339e5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="339e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339e5-132">-WhatIf</span></span>
<span data-ttu-id="339e5-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="339e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339e5-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="339e5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339e5-135">CommonParameters</span></span>
<span data-ttu-id="339e5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="339e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339e5-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="339e5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339e5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="339e5-138">INPUTS</span></span>

### <span data-ttu-id="339e5-139">System.object</span><span class="sxs-lookup"><span data-stu-id="339e5-139">System.String</span></span>
<span data-ttu-id="339e5-140">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="339e5-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="339e5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="339e5-141">OUTPUTS</span></span>

### <span data-ttu-id="339e5-142">PSRunCommandResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="339e5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="339e5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="339e5-143">NOTES</span></span>

## <span data-ttu-id="339e5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="339e5-144">RELATED LINKS</span></span>
