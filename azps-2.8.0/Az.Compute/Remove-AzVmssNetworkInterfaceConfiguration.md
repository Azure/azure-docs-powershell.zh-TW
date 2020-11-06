---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 58029017f4a6a272856f7badd6b09a9ba1f37ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613215"
---
# <span data-ttu-id="c5e60-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5e60-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c5e60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5e60-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e60-103">從 VMSS 中移除網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="c5e60-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="c5e60-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5e60-104">SYNTAX</span></span>

### <span data-ttu-id="c5e60-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5e60-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e60-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5e60-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e60-107">說明</span><span class="sxs-lookup"><span data-stu-id="c5e60-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e60-108">**AzVmssNetworkInterfaceConfiguration** Cmdlet 會從虛擬電腦規模集 (VMSS) 中移除網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="c5e60-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c5e60-109">示例</span><span class="sxs-lookup"><span data-stu-id="c5e60-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e60-110">範例1：移除介面配置</span><span class="sxs-lookup"><span data-stu-id="c5e60-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="c5e60-111">第一個命令會使用 Get-AzVmss Cmdlet 來取得 VMSS，然後將它儲存在 $VMSS 變數中。</span><span class="sxs-lookup"><span data-stu-id="c5e60-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="c5e60-112">第二個命令會從 $VMSS 的集合中移除名為 ContosoVmssInterface02 的網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="c5e60-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="c5e60-113">參數</span><span class="sxs-lookup"><span data-stu-id="c5e60-113">PARAMETERS</span></span>

### <span data-ttu-id="c5e60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e60-114">-DefaultProfile</span></span>
<span data-ttu-id="c5e60-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5e60-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e60-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c5e60-116">-Id</span></span>
<span data-ttu-id="c5e60-117">指定此 Cmdlet 移除之網路介面設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="c5e60-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5e60-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5e60-118">-Name</span></span>
<span data-ttu-id="c5e60-119">指定此 Cmdlet 移除的網路介面配置名稱。</span><span class="sxs-lookup"><span data-stu-id="c5e60-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5e60-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c5e60-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c5e60-121">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="c5e60-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="c5e60-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c5e60-122">-Confirm</span></span>
<span data-ttu-id="c5e60-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c5e60-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e60-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e60-124">-WhatIf</span></span>
<span data-ttu-id="c5e60-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5e60-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5e60-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5e60-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e60-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e60-127">CommonParameters</span></span>
<span data-ttu-id="c5e60-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5e60-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e60-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c5e60-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e60-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c5e60-130">INPUTS</span></span>

### <span data-ttu-id="c5e60-131">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c5e60-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c5e60-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c5e60-132">System.String</span></span>

## <span data-ttu-id="c5e60-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c5e60-133">OUTPUTS</span></span>

### <span data-ttu-id="c5e60-134">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c5e60-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c5e60-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c5e60-135">NOTES</span></span>

## <span data-ttu-id="c5e60-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5e60-136">RELATED LINKS</span></span>

[<span data-ttu-id="c5e60-137">附加 AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5e60-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="c5e60-138">AzVmss</span><span class="sxs-lookup"><span data-stu-id="c5e60-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


