---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: f77e018f464ffe7329d8b89cb74b8c44359d8a3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444687"
---
# <span data-ttu-id="ba5c7-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ba5c7-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="ba5c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5c7-103">設定 VMSS 的輪流升級原則屬性。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba5c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba5c7-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba5c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5c7-106">設定 VMSS 的輪流升級原則屬性。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="ba5c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="ba5c7-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5c7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ba5c7-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="ba5c7-109">這個命令會將 40 MaxBatchInstance、35% （MaxUnhealthyInstance）、MaxUnhealthyUpgradedInstance 的30%，以及 VMSS 局部物件 $vmss 的批次處理間暫停時間。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="ba5c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba5c7-110">PARAMETERS</span></span>

### <span data-ttu-id="ba5c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5c7-111">-DefaultProfile</span></span>
<span data-ttu-id="ba5c7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ba5c7-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="ba5c7-114">輪流升級在一批中同時升級之總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="ba5c7-115">如此一來，在前一個或將來的批次中，可能會導致批次中的實例百分比下降，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="ba5c7-116">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ba5c7-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="ba5c7-118">在輪流升級中止前，規模集中可同時進行升級的虛擬機器實例總數，或由虛擬機器健康情況檢查所顯示的總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="ba5c7-119">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="ba5c7-120">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ba5c7-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="ba5c7-122">可發現處於不正常狀態之已升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="ba5c7-123">這項檢查會在每個批次升級後發生。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="ba5c7-124">如果曾經超過此百分比，則滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="ba5c7-125">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="ba5c7-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="ba5c7-127">在一批中完成所有虛擬機器的更新與開始下一個批次之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="ba5c7-128">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="ba5c7-129">預設值為0秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ba5c7-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ba5c7-131">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="ba5c7-132">您可以使用 New-AzureRmVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ba5c7-133">-Confirm</span></span>
<span data-ttu-id="ba5c7-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5c7-135">-WhatIf</span></span>
<span data-ttu-id="ba5c7-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5c7-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5c7-138">CommonParameters</span></span>
<span data-ttu-id="ba5c7-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5c7-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5c7-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ba5c7-141">INPUTS</span></span>

### <span data-ttu-id="ba5c7-142">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="ba5c7-143">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]] System. 字串</span><span class="sxs-lookup"><span data-stu-id="ba5c7-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="ba5c7-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ba5c7-144">OUTPUTS</span></span>

### <span data-ttu-id="ba5c7-145">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ba5c7-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ba5c7-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ba5c7-146">NOTES</span></span>

## <span data-ttu-id="ba5c7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba5c7-147">RELATED LINKS</span></span>
