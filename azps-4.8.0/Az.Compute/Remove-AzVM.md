---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127117"
---
# <span data-ttu-id="85664-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-101">Remove-AzVM</span></span>

## <span data-ttu-id="85664-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85664-102">SYNOPSIS</span></span>
<span data-ttu-id="85664-103">從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85664-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="85664-104">句法</span><span class="sxs-lookup"><span data-stu-id="85664-104">SYNTAX</span></span>

### <span data-ttu-id="85664-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="85664-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85664-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="85664-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85664-107">說明</span><span class="sxs-lookup"><span data-stu-id="85664-107">DESCRIPTION</span></span>
<span data-ttu-id="85664-108">**AzVM** Cmdlet 會從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85664-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="85664-109">示例</span><span class="sxs-lookup"><span data-stu-id="85664-109">EXAMPLES</span></span>

### <span data-ttu-id="85664-110">範例1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="85664-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="85664-111">這個命令會從 [資源群組 ResourceGroup11] 中移除名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85664-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="85664-112">參數</span><span class="sxs-lookup"><span data-stu-id="85664-112">PARAMETERS</span></span>

### <span data-ttu-id="85664-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85664-113">-AsJob</span></span>
<span data-ttu-id="85664-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="85664-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="85664-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85664-115">-DefaultProfile</span></span>
<span data-ttu-id="85664-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85664-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85664-117">-Force</span><span class="sxs-lookup"><span data-stu-id="85664-117">-Force</span></span>
<span data-ttu-id="85664-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="85664-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85664-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="85664-119">-Id</span></span>
<span data-ttu-id="85664-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85664-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85664-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="85664-121">-Name</span></span>
<span data-ttu-id="85664-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="85664-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85664-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85664-123">-NoWait</span></span>
<span data-ttu-id="85664-124">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="85664-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="85664-125">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="85664-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="85664-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85664-126">-ResourceGroupName</span></span>
<span data-ttu-id="85664-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85664-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85664-128">-確認</span><span class="sxs-lookup"><span data-stu-id="85664-128">-Confirm</span></span>
<span data-ttu-id="85664-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85664-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85664-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85664-130">-WhatIf</span></span>
<span data-ttu-id="85664-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85664-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85664-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85664-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85664-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85664-133">CommonParameters</span></span>
<span data-ttu-id="85664-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85664-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85664-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="85664-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85664-136">輸入</span><span class="sxs-lookup"><span data-stu-id="85664-136">INPUTS</span></span>

### <span data-ttu-id="85664-137">System.object</span><span class="sxs-lookup"><span data-stu-id="85664-137">System.String</span></span>

## <span data-ttu-id="85664-138">輸出</span><span class="sxs-lookup"><span data-stu-id="85664-138">OUTPUTS</span></span>

### <span data-ttu-id="85664-139">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="85664-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="85664-140">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="85664-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="85664-141">筆記</span><span class="sxs-lookup"><span data-stu-id="85664-141">NOTES</span></span>

## <span data-ttu-id="85664-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="85664-142">RELATED LINKS</span></span>

[<span data-ttu-id="85664-143">AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="85664-144">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="85664-145">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="85664-146">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="85664-147">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="85664-148">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="85664-148">Update-AzVM</span></span>](./Update-AzVM.md)


