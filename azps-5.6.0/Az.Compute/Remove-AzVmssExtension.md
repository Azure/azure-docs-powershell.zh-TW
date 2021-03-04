---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 35a8ca7832727bef41d588a5551ae1f3efc86180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916433"
---
# <span data-ttu-id="1a5a7-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1a5a7-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="1a5a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5a7-103">從 VMSS 移除擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="1a5a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a5a7-104">SYNTAX</span></span>

### <span data-ttu-id="1a5a7-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a5a7-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a5a7-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a5a7-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a5a7-107">描述</span><span class="sxs-lookup"><span data-stu-id="1a5a7-107">DESCRIPTION</span></span>
<span data-ttu-id="1a5a7-108">**Remove-Az VmssExtension** Cmdlet 會從 VMSS (虛擬機器縮放集移除) 。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1a5a7-109">例子</span><span class="sxs-lookup"><span data-stu-id="1a5a7-109">EXAMPLES</span></span>

### <span data-ttu-id="1a5a7-110">範例 1：移除 VMSS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="1a5a7-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="1a5a7-111">此命令會移除 VMSS 的擴充功能，並更新修改後的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="1a5a7-112">範例 2：從 VMSS 移除實例</span><span class="sxs-lookup"><span data-stu-id="1a5a7-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="1a5a7-113">此命令會從屬於 Group002 資源群組的 VMSS 移除指定副檔名識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="1a5a7-114">參數</span><span class="sxs-lookup"><span data-stu-id="1a5a7-114">PARAMETERS</span></span>

### <span data-ttu-id="1a5a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5a7-115">-DefaultProfile</span></span>
<span data-ttu-id="1a5a7-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a5a7-117">-Id</span><span class="sxs-lookup"><span data-stu-id="1a5a7-117">-Id</span></span>
<span data-ttu-id="1a5a7-118">指定此 Cmdlet 從 VMSS 移除的擴充功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="1a5a7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a5a7-119">-Name</span></span>
<span data-ttu-id="1a5a7-120">指定此 Cmdlet 從 VMSS 移除的副檔名。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="1a5a7-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a5a7-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1a5a7-122">指定要從移除副檔名的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="1a5a7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1a5a7-123">-Confirm</span></span>
<span data-ttu-id="1a5a7-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a5a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a5a7-125">-WhatIf</span></span>
<span data-ttu-id="1a5a7-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a5a7-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a5a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5a7-128">CommonParameters</span></span>
<span data-ttu-id="1a5a7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a5a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5a7-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a5a7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5a7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1a5a7-131">INPUTS</span></span>

### <span data-ttu-id="1a5a7-132">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a5a7-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1a5a7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1a5a7-133">System.String</span></span>

## <span data-ttu-id="1a5a7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1a5a7-134">OUTPUTS</span></span>

### <span data-ttu-id="1a5a7-135">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a5a7-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1a5a7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1a5a7-136">NOTES</span></span>

## <span data-ttu-id="1a5a7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a5a7-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a5a7-138">Add-AzEvssExtension</span><span class="sxs-lookup"><span data-stu-id="1a5a7-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
