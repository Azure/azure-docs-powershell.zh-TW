---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: d5ce1af197575f96fd21f5355c0edfb98e3b181f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908614"
---
# <span data-ttu-id="82e30-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="82e30-101">Remove-AzVM</span></span>

## <span data-ttu-id="82e30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="82e30-102">SYNOPSIS</span></span>
<span data-ttu-id="82e30-103">從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="82e30-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="82e30-104">語法</span><span class="sxs-lookup"><span data-stu-id="82e30-104">SYNTAX</span></span>

### <span data-ttu-id="82e30-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="82e30-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e30-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82e30-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82e30-107">描述</span><span class="sxs-lookup"><span data-stu-id="82e30-107">DESCRIPTION</span></span>
<span data-ttu-id="82e30-108">**Remove-AzMS** Cmdlet 會從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="82e30-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="82e30-109">例子</span><span class="sxs-lookup"><span data-stu-id="82e30-109">EXAMPLES</span></span>

### <span data-ttu-id="82e30-110">範例 1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="82e30-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="82e30-111">此命令會移除資源群組 ResourceGroup11 中名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="82e30-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="82e30-112">參數</span><span class="sxs-lookup"><span data-stu-id="82e30-112">PARAMETERS</span></span>

### <span data-ttu-id="82e30-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82e30-113">-AsJob</span></span>
<span data-ttu-id="82e30-114">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="82e30-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="82e30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e30-115">-DefaultProfile</span></span>
<span data-ttu-id="82e30-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="82e30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82e30-117">-強制</span><span class="sxs-lookup"><span data-stu-id="82e30-117">-Force</span></span>
<span data-ttu-id="82e30-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="82e30-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82e30-119">-Id</span><span class="sxs-lookup"><span data-stu-id="82e30-119">-Id</span></span>
<span data-ttu-id="82e30-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="82e30-120">The resource group name.</span></span>

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

### <span data-ttu-id="82e30-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="82e30-121">-Name</span></span>
<span data-ttu-id="82e30-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="82e30-122">The resource name.</span></span>

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

### <span data-ttu-id="82e30-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82e30-123">-NoWait</span></span>
<span data-ttu-id="82e30-124">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="82e30-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="82e30-125">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="82e30-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="82e30-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e30-126">-ResourceGroupName</span></span>
<span data-ttu-id="82e30-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82e30-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="82e30-128">-確認</span><span class="sxs-lookup"><span data-stu-id="82e30-128">-Confirm</span></span>
<span data-ttu-id="82e30-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="82e30-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e30-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e30-130">-WhatIf</span></span>
<span data-ttu-id="82e30-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82e30-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82e30-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82e30-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e30-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e30-133">CommonParameters</span></span>
<span data-ttu-id="82e30-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="82e30-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e30-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82e30-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e30-136">輸入</span><span class="sxs-lookup"><span data-stu-id="82e30-136">INPUTS</span></span>

### <span data-ttu-id="82e30-137">System.String</span><span class="sxs-lookup"><span data-stu-id="82e30-137">System.String</span></span>

## <span data-ttu-id="82e30-138">輸出</span><span class="sxs-lookup"><span data-stu-id="82e30-138">OUTPUTS</span></span>

### <span data-ttu-id="82e30-139">Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="82e30-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="82e30-140">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="82e30-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="82e30-141">筆記</span><span class="sxs-lookup"><span data-stu-id="82e30-141">NOTES</span></span>

## <span data-ttu-id="82e30-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="82e30-142">RELATED LINKS</span></span>

[<span data-ttu-id="82e30-143">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="82e30-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="82e30-144">New-AzMS</span><span class="sxs-lookup"><span data-stu-id="82e30-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="82e30-145">Restart-AzMS</span><span class="sxs-lookup"><span data-stu-id="82e30-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="82e30-146">Start-AzMS</span><span class="sxs-lookup"><span data-stu-id="82e30-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="82e30-147">Stop-AzMS</span><span class="sxs-lookup"><span data-stu-id="82e30-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="82e30-148">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="82e30-148">Update-AzVM</span></span>](./Update-AzVM.md)


