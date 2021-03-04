---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903642"
---
# <span data-ttu-id="8425a-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="8425a-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="8425a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8425a-102">SYNOPSIS</span></span>
<span data-ttu-id="8425a-103">設定 VMSS 輪流升級策略屬性。</span><span class="sxs-lookup"><span data-stu-id="8425a-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="8425a-104">語法</span><span class="sxs-lookup"><span data-stu-id="8425a-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8425a-105">描述</span><span class="sxs-lookup"><span data-stu-id="8425a-105">DESCRIPTION</span></span>
<span data-ttu-id="8425a-106">設定 VMSS 輪流升級策略屬性。</span><span class="sxs-lookup"><span data-stu-id="8425a-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="8425a-107">例子</span><span class="sxs-lookup"><span data-stu-id="8425a-107">EXAMPLES</span></span>

### <span data-ttu-id="8425a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8425a-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="8425a-109">此命令會設定 MaxBatchInstance 的 40%，MaxUnhealthyInstance 的 35%，MaxUnhealthyUpgradedInstance 的 30%，以及 VMSS local object $vmss 批次之間的第二個暫停時間。</span><span class="sxs-lookup"><span data-stu-id="8425a-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="8425a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8425a-110">PARAMETERS</span></span>

### <span data-ttu-id="8425a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8425a-111">-DefaultProfile</span></span>
<span data-ttu-id="8425a-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8425a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8425a-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="8425a-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="8425a-114">在一個批次中以輪流升級同時升級的虛擬機器實例總數百分比上限。</span><span class="sxs-lookup"><span data-stu-id="8425a-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="8425a-115">由於這是上限，先前或未來批次中的不健康實例可能會導致批次中實例的百分比降低，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="8425a-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="8425a-116">如果未指定值，則值會設為 20。</span><span class="sxs-lookup"><span data-stu-id="8425a-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8425a-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="8425a-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="8425a-118">縮放集內同時不健康之虛擬機器實例總數的最大百分比，可能是升級的結果，或是由虛擬機器健康情況檢查在輪流升級中止之前發現處於不健康狀態。</span><span class="sxs-lookup"><span data-stu-id="8425a-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="8425a-119">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="8425a-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="8425a-120">如果未指定值，則值會設為 20。</span><span class="sxs-lookup"><span data-stu-id="8425a-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8425a-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="8425a-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="8425a-122">升級的虛擬機器實例百分比上限，可發現這些實例處於不健康狀態。</span><span class="sxs-lookup"><span data-stu-id="8425a-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="8425a-123">此檢查將在每個批次升級之後執行。</span><span class="sxs-lookup"><span data-stu-id="8425a-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="8425a-124">如果超過此百分比，滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="8425a-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="8425a-125">如果未指定值，則值會設為 20。</span><span class="sxs-lookup"><span data-stu-id="8425a-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8425a-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="8425a-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="8425a-127">在一個批次中完成所有虛擬機器的更新，到下一個批次開始之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="8425a-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="8425a-128">時間長度應該以 ISO 8601 格式指定。</span><span class="sxs-lookup"><span data-stu-id="8425a-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="8425a-129">預設值為 0 秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="8425a-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8425a-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8425a-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8425a-131">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="8425a-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="8425a-132">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="8425a-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8425a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8425a-133">-Confirm</span></span>
<span data-ttu-id="8425a-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8425a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8425a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8425a-135">-WhatIf</span></span>
<span data-ttu-id="8425a-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8425a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8425a-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8425a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8425a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8425a-138">CommonParameters</span></span>
<span data-ttu-id="8425a-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8425a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8425a-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8425a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8425a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8425a-141">INPUTS</span></span>

### <span data-ttu-id="8425a-142">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8425a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8425a-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8425a-143">System.Int32</span></span>

### <span data-ttu-id="8425a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8425a-144">System.String</span></span>

## <span data-ttu-id="8425a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8425a-145">OUTPUTS</span></span>

### <span data-ttu-id="8425a-146">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8425a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8425a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8425a-147">NOTES</span></span>

## <span data-ttu-id="8425a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8425a-148">RELATED LINKS</span></span>
