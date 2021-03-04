---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: eca73d71d213b31c0bbc339708cc744b3bf64d2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904734"
---
# <span data-ttu-id="492ef-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="492ef-101">Restart-AzVM</span></span>

## <span data-ttu-id="492ef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="492ef-102">SYNOPSIS</span></span>
<span data-ttu-id="492ef-103">重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="492ef-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="492ef-104">語法</span><span class="sxs-lookup"><span data-stu-id="492ef-104">SYNTAX</span></span>

### <span data-ttu-id="492ef-105">RestartResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="492ef-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="492ef-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="492ef-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="492ef-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="492ef-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="492ef-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="492ef-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="492ef-109">描述</span><span class="sxs-lookup"><span data-stu-id="492ef-109">DESCRIPTION</span></span>
<span data-ttu-id="492ef-110">**Restart-AzCMdlet** 會重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="492ef-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="492ef-111">例子</span><span class="sxs-lookup"><span data-stu-id="492ef-111">EXAMPLES</span></span>

### <span data-ttu-id="492ef-112">範例 1：重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="492ef-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="492ef-113">此命令會重新開機 ResourceGroup11 中名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="492ef-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="492ef-114">參數</span><span class="sxs-lookup"><span data-stu-id="492ef-114">PARAMETERS</span></span>

### <span data-ttu-id="492ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="492ef-115">-AsJob</span></span>
<span data-ttu-id="492ef-116">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="492ef-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="492ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492ef-117">-DefaultProfile</span></span>
<span data-ttu-id="492ef-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="492ef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="492ef-119">-Id</span><span class="sxs-lookup"><span data-stu-id="492ef-119">-Id</span></span>
<span data-ttu-id="492ef-120">虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="492ef-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="492ef-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="492ef-121">-Name</span></span>
<span data-ttu-id="492ef-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="492ef-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="492ef-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="492ef-123">-NoWait</span></span>
<span data-ttu-id="492ef-124">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="492ef-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="492ef-125">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="492ef-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="492ef-126">-執行Maintenance</span><span class="sxs-lookup"><span data-stu-id="492ef-126">-PerformMaintenance</span></span>
<span data-ttu-id="492ef-127">執行虛擬機器的維護。</span><span class="sxs-lookup"><span data-stu-id="492ef-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="492ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="492ef-129">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="492ef-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="492ef-130">-確認</span><span class="sxs-lookup"><span data-stu-id="492ef-130">-Confirm</span></span>
<span data-ttu-id="492ef-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="492ef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="492ef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="492ef-132">-WhatIf</span></span>
<span data-ttu-id="492ef-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="492ef-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="492ef-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="492ef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="492ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492ef-135">CommonParameters</span></span>
<span data-ttu-id="492ef-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="492ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492ef-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="492ef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492ef-138">輸入</span><span class="sxs-lookup"><span data-stu-id="492ef-138">INPUTS</span></span>

### <span data-ttu-id="492ef-139">System.String</span><span class="sxs-lookup"><span data-stu-id="492ef-139">System.String</span></span>

### <span data-ttu-id="492ef-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="492ef-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="492ef-141">輸出</span><span class="sxs-lookup"><span data-stu-id="492ef-141">OUTPUTS</span></span>

### <span data-ttu-id="492ef-142">Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="492ef-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="492ef-143">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="492ef-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="492ef-144">筆記</span><span class="sxs-lookup"><span data-stu-id="492ef-144">NOTES</span></span>

## <span data-ttu-id="492ef-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="492ef-145">RELATED LINKS</span></span>

[<span data-ttu-id="492ef-146">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="492ef-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="492ef-147">New-AzMS</span><span class="sxs-lookup"><span data-stu-id="492ef-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="492ef-148">Remove-AzMS</span><span class="sxs-lookup"><span data-stu-id="492ef-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="492ef-149">Start-AzMS</span><span class="sxs-lookup"><span data-stu-id="492ef-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="492ef-150">Stop-AzMS</span><span class="sxs-lookup"><span data-stu-id="492ef-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="492ef-151">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="492ef-151">Update-AzVM</span></span>](./Update-AzVM.md)


