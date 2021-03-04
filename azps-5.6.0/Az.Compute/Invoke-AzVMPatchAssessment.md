---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910281"
---
# <span data-ttu-id="3a7e8-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="3a7e8-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="3a7e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7e8-103">評估虛擬機器的修補狀態。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="3a7e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a7e8-104">SYNTAX</span></span>

### <span data-ttu-id="3a7e8-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3a7e8-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a7e8-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7e8-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a7e8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7e8-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a7e8-108">描述</span><span class="sxs-lookup"><span data-stu-id="3a7e8-108">DESCRIPTION</span></span>
<span data-ttu-id="3a7e8-109">評估 VM 的修補程式狀態，並報告可供安裝的所有偵測到的修補程式。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="3a7e8-110">例子</span><span class="sxs-lookup"><span data-stu-id="3a7e8-110">EXAMPLES</span></span>

### <span data-ttu-id="3a7e8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3a7e8-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="3a7e8-112">參數</span><span class="sxs-lookup"><span data-stu-id="3a7e8-112">PARAMETERS</span></span>

### <span data-ttu-id="3a7e8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a7e8-113">-AsJob</span></span>
<span data-ttu-id="3a7e8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3a7e8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a7e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7e8-115">-DefaultProfile</span></span>
<span data-ttu-id="3a7e8-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a7e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a7e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a7e8-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a7e8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a7e8-119">-ResourceId</span></span>
<span data-ttu-id="3a7e8-120">虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="3a7e8-121">-VM</span><span class="sxs-lookup"><span data-stu-id="3a7e8-121">-VM</span></span>
<span data-ttu-id="3a7e8-122">PowerShell 虛擬機器物件</span><span class="sxs-lookup"><span data-stu-id="3a7e8-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="3a7e8-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a7e8-123">-VMName</span></span>
<span data-ttu-id="3a7e8-124">虛擬機器名稱</span><span class="sxs-lookup"><span data-stu-id="3a7e8-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="3a7e8-125">-確認</span><span class="sxs-lookup"><span data-stu-id="3a7e8-125">-Confirm</span></span>
<span data-ttu-id="3a7e8-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7e8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a7e8-127">-WhatIf</span></span>
<span data-ttu-id="3a7e8-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a7e8-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7e8-130">CommonParameters</span></span>
<span data-ttu-id="3a7e8-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a7e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7e8-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a7e8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7e8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3a7e8-133">INPUTS</span></span>

### <span data-ttu-id="3a7e8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3a7e8-134">System.String</span></span>

## <span data-ttu-id="3a7e8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="3a7e8-135">OUTPUTS</span></span>

### <span data-ttu-id="3a7e8-136">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachinePatchAssesmentResult</span><span class="sxs-lookup"><span data-stu-id="3a7e8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="3a7e8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="3a7e8-137">NOTES</span></span>

## <span data-ttu-id="3a7e8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a7e8-138">RELATED LINKS</span></span>
