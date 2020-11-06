---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 676584e1e6814a05ba1ab49bb7c751218a16d361
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613217"
---
# <span data-ttu-id="f8eb9-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f8eb9-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="f8eb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="f8eb9-103">從 VMSS 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="f8eb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8eb9-104">SYNTAX</span></span>

### <span data-ttu-id="f8eb9-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8eb9-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8eb9-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8eb9-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8eb9-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8eb9-107">DESCRIPTION</span></span>
<span data-ttu-id="f8eb9-108">**AzVmssExtension** Cmdlet 會從虛擬電腦縮放集 (VMSS) 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f8eb9-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8eb9-109">EXAMPLES</span></span>

### <span data-ttu-id="f8eb9-110">範例1：移除 VMSS 延伸</span><span class="sxs-lookup"><span data-stu-id="f8eb9-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="f8eb9-111">這個命令會移除 VMSS 的延伸，並在修改之後更新 VMSS。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="f8eb9-112">範例2：從 VMSS 中移除實例</span><span class="sxs-lookup"><span data-stu-id="f8eb9-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="f8eb9-113">這個命令會從屬於名為 Group002 的資源群組的 VMSS 中，移除指定副檔名 id。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="f8eb9-114">參數</span><span class="sxs-lookup"><span data-stu-id="f8eb9-114">PARAMETERS</span></span>

### <span data-ttu-id="f8eb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8eb9-115">-DefaultProfile</span></span>
<span data-ttu-id="f8eb9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8eb9-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f8eb9-117">-Id</span></span>
<span data-ttu-id="f8eb9-118">指定此 Cmdlet 從 VMSS 移除的延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8eb9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8eb9-119">-Name</span></span>
<span data-ttu-id="f8eb9-120">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="f8eb9-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f8eb9-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f8eb9-122">指定要從中移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="f8eb9-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f8eb9-123">-Confirm</span></span>
<span data-ttu-id="f8eb9-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8eb9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8eb9-125">-WhatIf</span></span>
<span data-ttu-id="f8eb9-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8eb9-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8eb9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8eb9-128">CommonParameters</span></span>
<span data-ttu-id="f8eb9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8eb9-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8eb9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f8eb9-131">INPUTS</span></span>

### <span data-ttu-id="f8eb9-132">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f8eb9-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f8eb9-133">System.String</span></span>

## <span data-ttu-id="f8eb9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f8eb9-134">OUTPUTS</span></span>

### <span data-ttu-id="f8eb9-135">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f8eb9-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f8eb9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f8eb9-136">NOTES</span></span>

## <span data-ttu-id="f8eb9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8eb9-137">RELATED LINKS</span></span>

[<span data-ttu-id="f8eb9-138">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f8eb9-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
