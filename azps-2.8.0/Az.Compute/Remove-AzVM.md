---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 9256828a338678cb1da12e14cb6e450ee4030ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613252"
---
# <span data-ttu-id="9ed67-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-101">Remove-AzVM</span></span>

## <span data-ttu-id="9ed67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ed67-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed67-103">從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9ed67-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="9ed67-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ed67-104">SYNTAX</span></span>

### <span data-ttu-id="9ed67-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="9ed67-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed67-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9ed67-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed67-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ed67-107">DESCRIPTION</span></span>
<span data-ttu-id="9ed67-108">**AzVM** Cmdlet 會從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9ed67-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="9ed67-109">示例</span><span class="sxs-lookup"><span data-stu-id="9ed67-109">EXAMPLES</span></span>

### <span data-ttu-id="9ed67-110">範例1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="9ed67-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9ed67-111">這個命令會從 [資源群組 ResourceGroup11] 中移除名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9ed67-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="9ed67-112">參數</span><span class="sxs-lookup"><span data-stu-id="9ed67-112">PARAMETERS</span></span>

### <span data-ttu-id="9ed67-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ed67-113">-AsJob</span></span>
<span data-ttu-id="9ed67-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="9ed67-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9ed67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed67-115">-DefaultProfile</span></span>
<span data-ttu-id="9ed67-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ed67-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed67-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9ed67-117">-Force</span></span>
<span data-ttu-id="9ed67-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9ed67-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ed67-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9ed67-119">-Id</span></span>
<span data-ttu-id="9ed67-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed67-120">The resource group name.</span></span>

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

### <span data-ttu-id="9ed67-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ed67-121">-Name</span></span>
<span data-ttu-id="9ed67-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed67-122">The resource name.</span></span>

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

### <span data-ttu-id="9ed67-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9ed67-123">-NoWait</span></span>
<span data-ttu-id="9ed67-124">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="9ed67-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9ed67-125">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="9ed67-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9ed67-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed67-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ed67-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed67-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9ed67-128">-確認</span><span class="sxs-lookup"><span data-stu-id="9ed67-128">-Confirm</span></span>
<span data-ttu-id="9ed67-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ed67-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed67-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed67-130">-WhatIf</span></span>
<span data-ttu-id="9ed67-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ed67-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed67-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ed67-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed67-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed67-133">CommonParameters</span></span>
<span data-ttu-id="9ed67-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ed67-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed67-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ed67-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed67-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9ed67-136">INPUTS</span></span>

### <span data-ttu-id="9ed67-137">System.object</span><span class="sxs-lookup"><span data-stu-id="9ed67-137">System.String</span></span>

## <span data-ttu-id="9ed67-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9ed67-138">OUTPUTS</span></span>

### <span data-ttu-id="9ed67-139">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9ed67-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="9ed67-140">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9ed67-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9ed67-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9ed67-141">NOTES</span></span>

## <span data-ttu-id="9ed67-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ed67-142">RELATED LINKS</span></span>

[<span data-ttu-id="9ed67-143">AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9ed67-144">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="9ed67-145">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="9ed67-146">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="9ed67-147">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="9ed67-148">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ed67-148">Update-AzVM</span></span>](./Update-AzVM.md)

