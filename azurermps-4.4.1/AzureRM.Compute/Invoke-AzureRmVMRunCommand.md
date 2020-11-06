---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 2402591c6c388dbe7c1c6b24a1beb2b298012d4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457284"
---
# <span data-ttu-id="1868f-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="1868f-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="1868f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1868f-102">SYNOPSIS</span></span>
<span data-ttu-id="1868f-103">在 VM 上執行命令。</span><span class="sxs-lookup"><span data-stu-id="1868f-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1868f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1868f-104">SYNTAX</span></span>

### <span data-ttu-id="1868f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="1868f-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1868f-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="1868f-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1868f-107">說明</span><span class="sxs-lookup"><span data-stu-id="1868f-107">DESCRIPTION</span></span>
<span data-ttu-id="1868f-108">在 VM 上喚醒 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="1868f-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="1868f-109">示例</span><span class="sxs-lookup"><span data-stu-id="1868f-109">EXAMPLES</span></span>

### <span data-ttu-id="1868f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1868f-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="1868f-111">在資源群組 [rgname] 中，sample.ps1 使用 [vmname] 的 VM 中的 [RunPowerShellScript] 和 [VM] 中的參數，來喚醒呼叫 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="1868f-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="1868f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1868f-112">PARAMETERS</span></span>

### <span data-ttu-id="1868f-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="1868f-113">-CommandId</span></span>
<span data-ttu-id="1868f-114">[執行] 命令 id。</span><span class="sxs-lookup"><span data-stu-id="1868f-114">The run command id.</span></span>

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

### <span data-ttu-id="1868f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1868f-115">-DefaultProfile</span></span>
<span data-ttu-id="1868f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1868f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1868f-117">-參數</span><span class="sxs-lookup"><span data-stu-id="1868f-117">-Parameter</span></span>
<span data-ttu-id="1868f-118">Run 命令參數。</span><span class="sxs-lookup"><span data-stu-id="1868f-118">The run command parameters.</span></span>

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

### <span data-ttu-id="1868f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1868f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1868f-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1868f-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1868f-121">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="1868f-121">-ScriptPath</span></span>
<span data-ttu-id="1868f-122">要執行之腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="1868f-122">Path of the script to be executed.</span></span>  <span data-ttu-id="1868f-123">指定此值時，指定的腳本會覆寫命令的預設腳本。</span><span class="sxs-lookup"><span data-stu-id="1868f-123">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="1868f-124">-VM</span><span class="sxs-lookup"><span data-stu-id="1868f-124">-VM</span></span>
<span data-ttu-id="1868f-125">PS 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="1868f-125">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="1868f-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="1868f-126">-VMName</span></span>
<span data-ttu-id="1868f-127">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1868f-127">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1868f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1868f-128">-Confirm</span></span>
<span data-ttu-id="1868f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1868f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1868f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1868f-130">-WhatIf</span></span>
<span data-ttu-id="1868f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1868f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1868f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1868f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1868f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1868f-133">CommonParameters</span></span>
<span data-ttu-id="1868f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1868f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1868f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1868f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1868f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1868f-136">INPUTS</span></span>

### <span data-ttu-id="1868f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1868f-137">System.String</span></span>
<span data-ttu-id="1868f-138">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1868f-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1868f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1868f-139">OUTPUTS</span></span>

### <span data-ttu-id="1868f-140">PSRunCommandResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1868f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="1868f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1868f-141">NOTES</span></span>

## <span data-ttu-id="1868f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1868f-142">RELATED LINKS</span></span>

