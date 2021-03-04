---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914158"
---
# <span data-ttu-id="237ea-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="237ea-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="237ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="237ea-102">SYNOPSIS</span></span>
<span data-ttu-id="237ea-103">從 VMSS 移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="237ea-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="237ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="237ea-104">SYNTAX</span></span>

### <span data-ttu-id="237ea-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="237ea-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="237ea-106"><a0/</a0/ <a1/</a1</span><span class="sxs-lookup"><span data-stu-id="237ea-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="237ea-107">描述</span><span class="sxs-lookup"><span data-stu-id="237ea-107">DESCRIPTION</span></span>
<span data-ttu-id="237ea-108">**Remove-Az VmssDataData Cmdlet** 會從虛擬機器縮放集或 VMSS 實例 (資料) 磁片。</span><span class="sxs-lookup"><span data-stu-id="237ea-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="237ea-109">例子</span><span class="sxs-lookup"><span data-stu-id="237ea-109">EXAMPLES</span></span>

### <span data-ttu-id="237ea-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="237ea-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="237ea-111">此命令會從 VMSS 物件移除名為 "Data在1" 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="237ea-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="237ea-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="237ea-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="237ea-113">此命令會從 VMSS 物件移除 0 之資料磁片。</span><span class="sxs-lookup"><span data-stu-id="237ea-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="237ea-114">參數</span><span class="sxs-lookup"><span data-stu-id="237ea-114">PARAMETERS</span></span>

### <span data-ttu-id="237ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237ea-115">-DefaultProfile</span></span>
<span data-ttu-id="237ea-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="237ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="237ea-117">-四分位</span><span class="sxs-lookup"><span data-stu-id="237ea-117">-Lun</span></span>
<span data-ttu-id="237ea-118">指定磁片的邏輯單位編號。</span><span class="sxs-lookup"><span data-stu-id="237ea-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237ea-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="237ea-119">-Name</span></span>
<span data-ttu-id="237ea-120">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="237ea-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237ea-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="237ea-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="237ea-122">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="237ea-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="237ea-123">-確認</span><span class="sxs-lookup"><span data-stu-id="237ea-123">-Confirm</span></span>
<span data-ttu-id="237ea-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="237ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="237ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="237ea-125">-WhatIf</span></span>
<span data-ttu-id="237ea-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="237ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="237ea-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="237ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="237ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237ea-128">CommonParameters</span></span>
<span data-ttu-id="237ea-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="237ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237ea-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="237ea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237ea-131">輸入</span><span class="sxs-lookup"><span data-stu-id="237ea-131">INPUTS</span></span>

### <span data-ttu-id="237ea-132">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="237ea-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="237ea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="237ea-133">System.String</span></span>

### <span data-ttu-id="237ea-134">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="237ea-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="237ea-135">輸出</span><span class="sxs-lookup"><span data-stu-id="237ea-135">OUTPUTS</span></span>

### <span data-ttu-id="237ea-136">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="237ea-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="237ea-137">筆記</span><span class="sxs-lookup"><span data-stu-id="237ea-137">NOTES</span></span>

## <span data-ttu-id="237ea-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="237ea-138">RELATED LINKS</span></span>
