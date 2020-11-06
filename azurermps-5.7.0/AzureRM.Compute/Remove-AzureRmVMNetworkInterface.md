---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444723"
---
# <span data-ttu-id="95917-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="95917-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="95917-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95917-102">SYNOPSIS</span></span>
<span data-ttu-id="95917-103">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="95917-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95917-104">句法</span><span class="sxs-lookup"><span data-stu-id="95917-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95917-105">說明</span><span class="sxs-lookup"><span data-stu-id="95917-105">DESCRIPTION</span></span>
<span data-ttu-id="95917-106">**AzureRmVMNetworkInterface** Cmdlet 會將網路介面從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="95917-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="95917-107">示例</span><span class="sxs-lookup"><span data-stu-id="95917-107">EXAMPLES</span></span>

## <span data-ttu-id="95917-108">參數</span><span class="sxs-lookup"><span data-stu-id="95917-108">PARAMETERS</span></span>

### <span data-ttu-id="95917-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="95917-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="95917-110">指定此 Cmdlet 移除的網路介面 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="95917-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95917-111">-VM</span><span class="sxs-lookup"><span data-stu-id="95917-111">-VM</span></span>
<span data-ttu-id="95917-112">指定此 Cmdlet 移除網路介面的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95917-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="95917-113">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95917-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95917-114">-確認</span><span class="sxs-lookup"><span data-stu-id="95917-114">-Confirm</span></span>
<span data-ttu-id="95917-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95917-115">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95917-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95917-116">-WhatIf</span></span>
<span data-ttu-id="95917-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95917-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95917-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95917-118">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95917-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95917-119">CommonParameters</span></span>
<span data-ttu-id="95917-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95917-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95917-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95917-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95917-122">輸入</span><span class="sxs-lookup"><span data-stu-id="95917-122">INPUTS</span></span>

### <span data-ttu-id="95917-123">所有</span><span class="sxs-lookup"><span data-stu-id="95917-123">None</span></span>
<span data-ttu-id="95917-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="95917-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95917-125">輸出</span><span class="sxs-lookup"><span data-stu-id="95917-125">OUTPUTS</span></span>

## <span data-ttu-id="95917-126">筆記</span><span class="sxs-lookup"><span data-stu-id="95917-126">NOTES</span></span>

## <span data-ttu-id="95917-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="95917-127">RELATED LINKS</span></span>

[<span data-ttu-id="95917-128">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95917-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


