---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 7ede92fa653fe04072b75ce03dd6928421e01c6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443960"
---
# <span data-ttu-id="abe29-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="abe29-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="abe29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abe29-102">SYNOPSIS</span></span>
<span data-ttu-id="abe29-103">從 VMSS 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="abe29-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abe29-104">句法</span><span class="sxs-lookup"><span data-stu-id="abe29-104">SYNTAX</span></span>

### <span data-ttu-id="abe29-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="abe29-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe29-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abe29-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe29-107">說明</span><span class="sxs-lookup"><span data-stu-id="abe29-107">DESCRIPTION</span></span>
<span data-ttu-id="abe29-108">**AzureRmVmssExtension** Cmdlet 會從虛擬電腦縮放集 (VMSS) 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="abe29-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="abe29-109">示例</span><span class="sxs-lookup"><span data-stu-id="abe29-109">EXAMPLES</span></span>

### <span data-ttu-id="abe29-110">範例1：移除 VMSS 延伸</span><span class="sxs-lookup"><span data-stu-id="abe29-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzureRmVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="abe29-111">這個命令會移除 VMSS 的延伸，並在修改之後更新 VMSS。</span><span class="sxs-lookup"><span data-stu-id="abe29-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="abe29-112">範例2：從 VMSS 中移除實例</span><span class="sxs-lookup"><span data-stu-id="abe29-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="abe29-113">這個命令會從屬於名為 Group002 的資源群組的 VMSS 中，移除指定副檔名 id。</span><span class="sxs-lookup"><span data-stu-id="abe29-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="abe29-114">參數</span><span class="sxs-lookup"><span data-stu-id="abe29-114">PARAMETERS</span></span>

### <span data-ttu-id="abe29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe29-115">-DefaultProfile</span></span>
<span data-ttu-id="abe29-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="abe29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abe29-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="abe29-117">-Id</span></span>
<span data-ttu-id="abe29-118">指定此 Cmdlet 從 VMSS 移除的延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="abe29-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="abe29-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="abe29-119">-Name</span></span>
<span data-ttu-id="abe29-120">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="abe29-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="abe29-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="abe29-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="abe29-122">指定要從中移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="abe29-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="abe29-123">-確認</span><span class="sxs-lookup"><span data-stu-id="abe29-123">-Confirm</span></span>
<span data-ttu-id="abe29-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="abe29-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe29-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe29-125">-WhatIf</span></span>
<span data-ttu-id="abe29-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abe29-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abe29-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abe29-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe29-128">CommonParameters</span></span>
<span data-ttu-id="abe29-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abe29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe29-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abe29-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe29-131">輸入</span><span class="sxs-lookup"><span data-stu-id="abe29-131">INPUTS</span></span>

### <span data-ttu-id="abe29-132">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="abe29-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="abe29-133">System.object</span><span class="sxs-lookup"><span data-stu-id="abe29-133">System.String</span></span>

## <span data-ttu-id="abe29-134">輸出</span><span class="sxs-lookup"><span data-stu-id="abe29-134">OUTPUTS</span></span>

### <span data-ttu-id="abe29-135">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="abe29-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="abe29-136">筆記</span><span class="sxs-lookup"><span data-stu-id="abe29-136">NOTES</span></span>

## <span data-ttu-id="abe29-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="abe29-137">RELATED LINKS</span></span>

[<span data-ttu-id="abe29-138">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="abe29-138">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
