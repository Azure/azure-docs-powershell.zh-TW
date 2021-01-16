---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283968"
---
# <span data-ttu-id="3e06d-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="3e06d-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="3e06d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e06d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e06d-103">評估虛擬機器的修補程式狀態。</span><span class="sxs-lookup"><span data-stu-id="3e06d-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="3e06d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e06d-104">SYNTAX</span></span>

### <span data-ttu-id="3e06d-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3e06d-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e06d-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e06d-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e06d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e06d-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e06d-108">說明</span><span class="sxs-lookup"><span data-stu-id="3e06d-108">DESCRIPTION</span></span>
<span data-ttu-id="3e06d-109">評估 VM 的修補程式狀態，並報告所有可供安裝的修補程式。</span><span class="sxs-lookup"><span data-stu-id="3e06d-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="3e06d-110">示例</span><span class="sxs-lookup"><span data-stu-id="3e06d-110">EXAMPLES</span></span>

### <span data-ttu-id="3e06d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3e06d-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="3e06d-112">參數</span><span class="sxs-lookup"><span data-stu-id="3e06d-112">PARAMETERS</span></span>

### <span data-ttu-id="3e06d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e06d-113">-AsJob</span></span>
<span data-ttu-id="3e06d-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3e06d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e06d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e06d-115">-DefaultProfile</span></span>
<span data-ttu-id="3e06d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e06d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e06d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e06d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e06d-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e06d-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e06d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e06d-119">-ResourceId</span></span>
<span data-ttu-id="3e06d-120">虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e06d-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e06d-121">-VM</span><span class="sxs-lookup"><span data-stu-id="3e06d-121">-VM</span></span>
<span data-ttu-id="3e06d-122">PowerShell 虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="3e06d-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e06d-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e06d-123">-VMName</span></span>
<span data-ttu-id="3e06d-124">虛擬機器名稱</span><span class="sxs-lookup"><span data-stu-id="3e06d-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e06d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="3e06d-125">-Confirm</span></span>
<span data-ttu-id="3e06d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e06d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e06d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e06d-127">-WhatIf</span></span>
<span data-ttu-id="3e06d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e06d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e06d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e06d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e06d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e06d-130">CommonParameters</span></span>
<span data-ttu-id="3e06d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e06d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e06d-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3e06d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e06d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3e06d-133">INPUTS</span></span>

### <span data-ttu-id="3e06d-134">System.object</span><span class="sxs-lookup"><span data-stu-id="3e06d-134">System.String</span></span>

## <span data-ttu-id="3e06d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="3e06d-135">OUTPUTS</span></span>

### <span data-ttu-id="3e06d-136">PSVirtualMachinePatchAssessmentResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3e06d-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="3e06d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="3e06d-137">NOTES</span></span>

## <span data-ttu-id="3e06d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e06d-138">RELATED LINKS</span></span>
