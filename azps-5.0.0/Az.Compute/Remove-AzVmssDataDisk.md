---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140200"
---
# <span data-ttu-id="f0172-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f0172-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="f0172-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0172-102">SYNOPSIS</span></span>
<span data-ttu-id="f0172-103">從 VMSS 中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f0172-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="f0172-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0172-104">SYNTAX</span></span>

### <span data-ttu-id="f0172-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0172-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0172-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0172-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0172-107">說明</span><span class="sxs-lookup"><span data-stu-id="f0172-107">DESCRIPTION</span></span>
<span data-ttu-id="f0172-108">**AzVmssDataDisk** Cmdlet 會從虛擬電腦規模集 (VMSS) 實例中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f0172-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f0172-109">示例</span><span class="sxs-lookup"><span data-stu-id="f0172-109">EXAMPLES</span></span>

### <span data-ttu-id="f0172-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f0172-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="f0172-111">這個命令會從 VMSS 物件中移除名為「DataDisk1」的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f0172-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="f0172-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f0172-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="f0172-113">這個命令會從 VMSS 物件中移除 LUN 0 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f0172-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="f0172-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0172-114">PARAMETERS</span></span>

### <span data-ttu-id="f0172-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0172-115">-DefaultProfile</span></span>
<span data-ttu-id="f0172-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0172-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0172-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="f0172-117">-Lun</span></span>
<span data-ttu-id="f0172-118">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="f0172-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="f0172-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0172-119">-Name</span></span>
<span data-ttu-id="f0172-120">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0172-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="f0172-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0172-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f0172-122">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="f0172-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="f0172-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f0172-123">-Confirm</span></span>
<span data-ttu-id="f0172-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0172-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0172-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0172-125">-WhatIf</span></span>
<span data-ttu-id="f0172-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0172-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0172-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0172-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0172-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0172-128">CommonParameters</span></span>
<span data-ttu-id="f0172-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0172-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0172-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0172-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0172-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f0172-131">INPUTS</span></span>

### <span data-ttu-id="f0172-132">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f0172-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f0172-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f0172-133">System.String</span></span>

### <span data-ttu-id="f0172-134">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0172-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f0172-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f0172-135">OUTPUTS</span></span>

### <span data-ttu-id="f0172-136">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f0172-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f0172-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f0172-137">NOTES</span></span>

## <span data-ttu-id="f0172-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0172-138">RELATED LINKS</span></span>
