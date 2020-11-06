---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448726"
---
# <span data-ttu-id="3e501-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e501-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="3e501-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e501-102">SYNOPSIS</span></span>
<span data-ttu-id="3e501-103">從 VMSS 中移除網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="3e501-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e501-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e501-104">SYNTAX</span></span>

### <span data-ttu-id="3e501-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e501-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e501-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e501-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e501-107">說明</span><span class="sxs-lookup"><span data-stu-id="3e501-107">DESCRIPTION</span></span>
<span data-ttu-id="3e501-108">**AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 會從虛擬電腦規模集 (VMSS) 中移除網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="3e501-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3e501-109">示例</span><span class="sxs-lookup"><span data-stu-id="3e501-109">EXAMPLES</span></span>

### <span data-ttu-id="3e501-110">範例1：移除介面配置</span><span class="sxs-lookup"><span data-stu-id="3e501-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="3e501-111">第一個命令會使用 Get-AzureRmVmss Cmdlet 來取得 VMSS，然後將它儲存在 $VMSS 變數中。</span><span class="sxs-lookup"><span data-stu-id="3e501-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="3e501-112">第二個命令會從 $VMSS 的集合中移除名為 ContosoVmssInterface02 的網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="3e501-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="3e501-113">參數</span><span class="sxs-lookup"><span data-stu-id="3e501-113">PARAMETERS</span></span>

### <span data-ttu-id="3e501-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="3e501-114">-Id</span></span>
<span data-ttu-id="3e501-115">指定此 Cmdlet 移除之網路介面設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="3e501-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e501-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e501-116">-Name</span></span>
<span data-ttu-id="3e501-117">指定此 Cmdlet 移除的網路介面配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3e501-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e501-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3e501-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3e501-119">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="3e501-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e501-120">-確認</span><span class="sxs-lookup"><span data-stu-id="3e501-120">-Confirm</span></span>
<span data-ttu-id="3e501-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e501-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e501-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e501-122">-WhatIf</span></span>
<span data-ttu-id="3e501-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e501-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e501-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e501-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e501-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e501-125">CommonParameters</span></span>
<span data-ttu-id="3e501-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e501-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e501-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e501-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e501-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3e501-128">INPUTS</span></span>

### <span data-ttu-id="3e501-129">所有</span><span class="sxs-lookup"><span data-stu-id="3e501-129">None</span></span>
<span data-ttu-id="3e501-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3e501-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e501-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3e501-131">OUTPUTS</span></span>

## <span data-ttu-id="3e501-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3e501-132">NOTES</span></span>

## <span data-ttu-id="3e501-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e501-133">RELATED LINKS</span></span>

[<span data-ttu-id="3e501-134">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e501-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="3e501-135">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3e501-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


