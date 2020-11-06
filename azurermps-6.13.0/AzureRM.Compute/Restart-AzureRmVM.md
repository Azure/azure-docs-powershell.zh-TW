---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447411"
---
# <span data-ttu-id="78a9a-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="78a9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="78a9a-103">重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="78a9a-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78a9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="78a9a-104">SYNTAX</span></span>

### <span data-ttu-id="78a9a-105">RestartResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="78a9a-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a9a-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="78a9a-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a9a-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="78a9a-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a9a-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="78a9a-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a9a-109">說明</span><span class="sxs-lookup"><span data-stu-id="78a9a-109">DESCRIPTION</span></span>
<span data-ttu-id="78a9a-110">**Restart AzureRmVM** Cmdlet 會重新開機 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="78a9a-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="78a9a-111">示例</span><span class="sxs-lookup"><span data-stu-id="78a9a-111">EXAMPLES</span></span>

### <span data-ttu-id="78a9a-112">範例1：重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="78a9a-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="78a9a-113">這個命令會在 ResourceGroup11 中重新開機名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="78a9a-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="78a9a-114">參數</span><span class="sxs-lookup"><span data-stu-id="78a9a-114">PARAMETERS</span></span>

### <span data-ttu-id="78a9a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78a9a-115">-AsJob</span></span>
<span data-ttu-id="78a9a-116">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="78a9a-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="78a9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a9a-117">-DefaultProfile</span></span>
<span data-ttu-id="78a9a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78a9a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a9a-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="78a9a-119">-Id</span></span>
<span data-ttu-id="78a9a-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78a9a-120">The resource group name.</span></span>

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

### <span data-ttu-id="78a9a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="78a9a-121">-Name</span></span>
<span data-ttu-id="78a9a-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="78a9a-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a9a-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="78a9a-123">-PerformMaintenance</span></span>
<span data-ttu-id="78a9a-124">執行虛擬機器的維護作業。</span><span class="sxs-lookup"><span data-stu-id="78a9a-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="78a9a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a9a-125">-ResourceGroupName</span></span>
<span data-ttu-id="78a9a-126">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78a9a-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="78a9a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="78a9a-127">-Confirm</span></span>
<span data-ttu-id="78a9a-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78a9a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a9a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a9a-129">-WhatIf</span></span>
<span data-ttu-id="78a9a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78a9a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78a9a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78a9a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a9a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a9a-132">CommonParameters</span></span>
<span data-ttu-id="78a9a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78a9a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a9a-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78a9a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a9a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="78a9a-135">INPUTS</span></span>

### <span data-ttu-id="78a9a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="78a9a-136">System.String</span></span>

### <span data-ttu-id="78a9a-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="78a9a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78a9a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="78a9a-138">OUTPUTS</span></span>

### <span data-ttu-id="78a9a-139">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="78a9a-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="78a9a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="78a9a-140">NOTES</span></span>

## <span data-ttu-id="78a9a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="78a9a-141">RELATED LINKS</span></span>

[<span data-ttu-id="78a9a-142">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="78a9a-143">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="78a9a-144">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="78a9a-145">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="78a9a-146">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="78a9a-147">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78a9a-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

