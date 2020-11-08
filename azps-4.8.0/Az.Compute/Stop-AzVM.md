---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127105"
---
# <span data-ttu-id="73793-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-101">Stop-AzVM</span></span>

## <span data-ttu-id="73793-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73793-102">SYNOPSIS</span></span>
<span data-ttu-id="73793-103">停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="73793-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="73793-104">句法</span><span class="sxs-lookup"><span data-stu-id="73793-104">SYNTAX</span></span>

### <span data-ttu-id="73793-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="73793-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73793-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="73793-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73793-107">說明</span><span class="sxs-lookup"><span data-stu-id="73793-107">DESCRIPTION</span></span>
<span data-ttu-id="73793-108">**AzVM** Cmdlet 會停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="73793-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="73793-109">示例</span><span class="sxs-lookup"><span data-stu-id="73793-109">EXAMPLES</span></span>

### <span data-ttu-id="73793-110">範例1：停止虛擬機器</span><span class="sxs-lookup"><span data-stu-id="73793-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="73793-111">這個命令會在 ResourceGroup11 中停止名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="73793-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="73793-112">參數</span><span class="sxs-lookup"><span data-stu-id="73793-112">PARAMETERS</span></span>

### <span data-ttu-id="73793-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73793-113">-AsJob</span></span>
<span data-ttu-id="73793-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="73793-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="73793-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73793-115">-DefaultProfile</span></span>
<span data-ttu-id="73793-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73793-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73793-117">-Force</span><span class="sxs-lookup"><span data-stu-id="73793-117">-Force</span></span>
<span data-ttu-id="73793-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="73793-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73793-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="73793-119">-Id</span></span>
<span data-ttu-id="73793-120">虛擬機器的 ID。</span><span class="sxs-lookup"><span data-stu-id="73793-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="73793-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="73793-121">-Name</span></span>
<span data-ttu-id="73793-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="73793-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73793-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="73793-123">-NoWait</span></span>
<span data-ttu-id="73793-124">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="73793-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="73793-125">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="73793-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="73793-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73793-126">-ResourceGroupName</span></span>
<span data-ttu-id="73793-127">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73793-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="73793-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="73793-128">-SkipShutdown</span></span>
<span data-ttu-id="73793-129">在保持 VM 已預配的情況下，要求不正常的 VM 關閉。</span><span class="sxs-lookup"><span data-stu-id="73793-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="73793-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="73793-130">-StayProvisioned</span></span>
<span data-ttu-id="73793-131">這個 Cmdlet 會停止 VMSS 中的所有虛擬機器，但不會解除配置。</span><span class="sxs-lookup"><span data-stu-id="73793-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="73793-132">帳戶會針對已停止的虛擬機器收取費用。</span><span class="sxs-lookup"><span data-stu-id="73793-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="73793-133">-確認</span><span class="sxs-lookup"><span data-stu-id="73793-133">-Confirm</span></span>
<span data-ttu-id="73793-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73793-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73793-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73793-135">-WhatIf</span></span>
<span data-ttu-id="73793-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73793-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73793-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73793-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73793-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73793-138">CommonParameters</span></span>
<span data-ttu-id="73793-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73793-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73793-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73793-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73793-141">輸入</span><span class="sxs-lookup"><span data-stu-id="73793-141">INPUTS</span></span>

### <span data-ttu-id="73793-142">System.object</span><span class="sxs-lookup"><span data-stu-id="73793-142">System.String</span></span>

## <span data-ttu-id="73793-143">輸出</span><span class="sxs-lookup"><span data-stu-id="73793-143">OUTPUTS</span></span>

### <span data-ttu-id="73793-144">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="73793-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="73793-145">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="73793-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="73793-146">筆記</span><span class="sxs-lookup"><span data-stu-id="73793-146">NOTES</span></span>

## <span data-ttu-id="73793-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="73793-147">RELATED LINKS</span></span>

[<span data-ttu-id="73793-148">AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="73793-149">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="73793-150">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="73793-151">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="73793-152">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="73793-153">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="73793-153">Update-AzVM</span></span>](./Update-AzVM.md)


