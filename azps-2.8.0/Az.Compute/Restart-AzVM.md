---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 8fe939bfb959a1a6bc2dc043dbc3948943aa2c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613209"
---
# <span data-ttu-id="ea554-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-101">Restart-AzVM</span></span>

## <span data-ttu-id="ea554-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea554-102">SYNOPSIS</span></span>
<span data-ttu-id="ea554-103">重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea554-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ea554-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea554-104">SYNTAX</span></span>

### <span data-ttu-id="ea554-105">RestartResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="ea554-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea554-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ea554-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea554-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ea554-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea554-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ea554-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea554-109">說明</span><span class="sxs-lookup"><span data-stu-id="ea554-109">DESCRIPTION</span></span>
<span data-ttu-id="ea554-110">**Restart AzVM** Cmdlet 會重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea554-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ea554-111">示例</span><span class="sxs-lookup"><span data-stu-id="ea554-111">EXAMPLES</span></span>

### <span data-ttu-id="ea554-112">範例1：重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea554-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ea554-113">這個命令會在 ResourceGroup11 中重新開機名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea554-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ea554-114">參數</span><span class="sxs-lookup"><span data-stu-id="ea554-114">PARAMETERS</span></span>

### <span data-ttu-id="ea554-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea554-115">-AsJob</span></span>
<span data-ttu-id="ea554-116">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ea554-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ea554-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea554-117">-DefaultProfile</span></span>
<span data-ttu-id="ea554-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea554-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea554-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ea554-119">-Id</span></span>
<span data-ttu-id="ea554-120">虛擬機器的 ID。</span><span class="sxs-lookup"><span data-stu-id="ea554-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ea554-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea554-121">-Name</span></span>
<span data-ttu-id="ea554-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="ea554-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="ea554-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea554-123">-NoWait</span></span>
<span data-ttu-id="ea554-124">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="ea554-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ea554-125">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="ea554-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ea554-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="ea554-126">-PerformMaintenance</span></span>
<span data-ttu-id="ea554-127">執行虛擬機器的維護作業。</span><span class="sxs-lookup"><span data-stu-id="ea554-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="ea554-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea554-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea554-129">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea554-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ea554-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ea554-130">-Confirm</span></span>
<span data-ttu-id="ea554-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea554-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea554-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea554-132">-WhatIf</span></span>
<span data-ttu-id="ea554-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea554-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea554-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea554-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea554-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea554-135">CommonParameters</span></span>
<span data-ttu-id="ea554-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea554-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea554-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ea554-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea554-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ea554-138">INPUTS</span></span>

### <span data-ttu-id="ea554-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ea554-139">System.String</span></span>

### <span data-ttu-id="ea554-140">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ea554-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea554-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ea554-141">OUTPUTS</span></span>

### <span data-ttu-id="ea554-142">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ea554-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="ea554-143">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ea554-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ea554-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ea554-144">NOTES</span></span>

## <span data-ttu-id="ea554-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea554-145">RELATED LINKS</span></span>

[<span data-ttu-id="ea554-146">AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ea554-147">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ea554-148">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="ea554-149">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ea554-150">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ea554-151">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="ea554-151">Update-AzVM</span></span>](./Update-AzVM.md)

