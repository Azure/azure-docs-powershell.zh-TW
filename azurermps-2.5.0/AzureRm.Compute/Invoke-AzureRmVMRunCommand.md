---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
ms.openlocfilehash: 12b9b3870b5239746a8524bad9aad0f44161acd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801413"
---
# <span data-ttu-id="7bfc9-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="7bfc9-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="7bfc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfc9-103">在 VM 上執行命令。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bfc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bfc9-104">SYNTAX</span></span>

### <span data-ttu-id="7bfc9-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="7bfc9-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bfc9-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="7bfc9-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bfc9-107">說明</span><span class="sxs-lookup"><span data-stu-id="7bfc9-107">DESCRIPTION</span></span>
<span data-ttu-id="7bfc9-108">在 VM 上喚醒 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="7bfc9-109">示例</span><span class="sxs-lookup"><span data-stu-id="7bfc9-109">EXAMPLES</span></span>

### <span data-ttu-id="7bfc9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7bfc9-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="7bfc9-111">在資源群組 [rgname] 中，sample.ps1 使用 [vmname] 的 VM 中的 [RunPowerShellScript] 和 [VM] 中的參數，來喚醒呼叫 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="7bfc9-112">參數</span><span class="sxs-lookup"><span data-stu-id="7bfc9-112">PARAMETERS</span></span>

### <span data-ttu-id="7bfc9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bfc9-113">-AsJob</span></span>
<span data-ttu-id="7bfc9-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7bfc9-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="7bfc9-115">-CommandId</span></span>
<span data-ttu-id="7bfc9-116">[執行] 命令 id。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-116">The run command id.</span></span>

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

### <span data-ttu-id="7bfc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfc9-117">-DefaultProfile</span></span>
<span data-ttu-id="7bfc9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bfc9-119">-參數</span><span class="sxs-lookup"><span data-stu-id="7bfc9-119">-Parameter</span></span>
<span data-ttu-id="7bfc9-120">Run 命令參數。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-120">The run command parameters.</span></span>

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

### <span data-ttu-id="7bfc9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bfc9-121">-ResourceGroupName</span></span>
<span data-ttu-id="7bfc9-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7bfc9-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="7bfc9-123">-ScriptPath</span></span>
<span data-ttu-id="7bfc9-124">要執行之腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-124">Path of the script to be executed.</span></span>  <span data-ttu-id="7bfc9-125">指定此值時，指定的腳本會覆寫命令的預設腳本。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="7bfc9-126">-VM</span><span class="sxs-lookup"><span data-stu-id="7bfc9-126">-VM</span></span>
<span data-ttu-id="7bfc9-127">PS 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="7bfc9-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="7bfc9-128">-VMName</span></span>
<span data-ttu-id="7bfc9-129">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="7bfc9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="7bfc9-130">-Confirm</span></span>
<span data-ttu-id="7bfc9-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bfc9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bfc9-132">-WhatIf</span></span>
<span data-ttu-id="7bfc9-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bfc9-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bfc9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfc9-135">CommonParameters</span></span>
<span data-ttu-id="7bfc9-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfc9-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfc9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7bfc9-138">INPUTS</span></span>

### <span data-ttu-id="7bfc9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7bfc9-139">System.String</span></span>
<span data-ttu-id="7bfc9-140">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7bfc9-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7bfc9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7bfc9-141">OUTPUTS</span></span>

### <span data-ttu-id="7bfc9-142">PSRunCommandResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7bfc9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="7bfc9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7bfc9-143">NOTES</span></span>

## <span data-ttu-id="7bfc9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bfc9-144">RELATED LINKS</span></span>

