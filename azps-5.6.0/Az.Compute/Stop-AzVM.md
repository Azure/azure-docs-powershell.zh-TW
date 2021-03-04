---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 36d86f701bfdeea67869b45512a79eeee45c0457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911746"
---
# <span data-ttu-id="7c5de-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7c5de-101">Stop-AzVM</span></span>

## <span data-ttu-id="7c5de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7c5de-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5de-103">停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c5de-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7c5de-104">語法</span><span class="sxs-lookup"><span data-stu-id="7c5de-104">SYNTAX</span></span>

### <span data-ttu-id="7c5de-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="7c5de-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c5de-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7c5de-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c5de-107">描述</span><span class="sxs-lookup"><span data-stu-id="7c5de-107">DESCRIPTION</span></span>
<span data-ttu-id="7c5de-108">**Stop-AzMS** Cmdlet 會停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c5de-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7c5de-109">例子</span><span class="sxs-lookup"><span data-stu-id="7c5de-109">EXAMPLES</span></span>

### <span data-ttu-id="7c5de-110">範例 1：停止虛擬機器</span><span class="sxs-lookup"><span data-stu-id="7c5de-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7c5de-111">此命令會停止 ResourceGroup11 中名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c5de-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7c5de-112">參數</span><span class="sxs-lookup"><span data-stu-id="7c5de-112">PARAMETERS</span></span>

### <span data-ttu-id="7c5de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c5de-113">-AsJob</span></span>
<span data-ttu-id="7c5de-114">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="7c5de-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7c5de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5de-115">-DefaultProfile</span></span>
<span data-ttu-id="7c5de-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c5de-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c5de-117">-強制</span><span class="sxs-lookup"><span data-stu-id="7c5de-117">-Force</span></span>
<span data-ttu-id="7c5de-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7c5de-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c5de-119">-Id</span><span class="sxs-lookup"><span data-stu-id="7c5de-119">-Id</span></span>
<span data-ttu-id="7c5de-120">虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c5de-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="7c5de-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c5de-121">-Name</span></span>
<span data-ttu-id="7c5de-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="7c5de-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="7c5de-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c5de-123">-NoWait</span></span>
<span data-ttu-id="7c5de-124">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="7c5de-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7c5de-125">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="7c5de-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7c5de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5de-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c5de-127">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7c5de-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7c5de-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="7c5de-128">-SkipShutdown</span></span>
<span data-ttu-id="7c5de-129">若要在保留部署 VM 時要求關閉非正常 VM。</span><span class="sxs-lookup"><span data-stu-id="7c5de-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="7c5de-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="7c5de-130">-StayProvisioned</span></span>
<span data-ttu-id="7c5de-131">Cmdlet 會停止 VMSS 內的所有虛擬機器，但不會解除配置。</span><span class="sxs-lookup"><span data-stu-id="7c5de-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="7c5de-132">該帳戶會針對已停止的虛擬機器收費。</span><span class="sxs-lookup"><span data-stu-id="7c5de-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="7c5de-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7c5de-133">-Confirm</span></span>
<span data-ttu-id="7c5de-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7c5de-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c5de-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c5de-135">-WhatIf</span></span>
<span data-ttu-id="7c5de-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c5de-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c5de-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c5de-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c5de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5de-138">CommonParameters</span></span>
<span data-ttu-id="7c5de-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7c5de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5de-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c5de-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5de-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7c5de-141">INPUTS</span></span>

### <span data-ttu-id="7c5de-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7c5de-142">System.String</span></span>

## <span data-ttu-id="7c5de-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7c5de-143">OUTPUTS</span></span>

### <span data-ttu-id="7c5de-144">Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7c5de-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="7c5de-145">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7c5de-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7c5de-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7c5de-146">NOTES</span></span>

## <span data-ttu-id="7c5de-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c5de-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c5de-148">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="7c5de-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7c5de-149">New-AzMS</span><span class="sxs-lookup"><span data-stu-id="7c5de-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7c5de-150">Remove-AzMS</span><span class="sxs-lookup"><span data-stu-id="7c5de-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7c5de-151">Restart-AzMS</span><span class="sxs-lookup"><span data-stu-id="7c5de-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7c5de-152">Start-AzMS</span><span class="sxs-lookup"><span data-stu-id="7c5de-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7c5de-153">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="7c5de-153">Update-AzVM</span></span>](./Update-AzVM.md)


