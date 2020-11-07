---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801390"
---
# <span data-ttu-id="b1ff8-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b1ff8-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="b1ff8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ff8-103">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1ff8-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1ff8-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1ff8-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="b1ff8-106">**AzureRmVMNetworkInterface** Cmdlet 會將網路介面從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="b1ff8-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="b1ff8-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="b1ff8-108">1:</span></span>
```

```

## <span data-ttu-id="b1ff8-109">參數</span><span class="sxs-lookup"><span data-stu-id="b1ff8-109">PARAMETERS</span></span>

### <span data-ttu-id="b1ff8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ff8-110">-DefaultProfile</span></span>
<span data-ttu-id="b1ff8-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1ff8-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="b1ff8-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="b1ff8-113">指定此 Cmdlet 移除的網路介面 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1ff8-114">-VM</span><span class="sxs-lookup"><span data-stu-id="b1ff8-114">-VM</span></span>
<span data-ttu-id="b1ff8-115">指定此 Cmdlet 移除網路介面的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="b1ff8-116">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="b1ff8-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b1ff8-117">-Confirm</span></span>
<span data-ttu-id="b1ff8-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="b1ff8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1ff8-119">-WhatIf</span></span>
<span data-ttu-id="b1ff8-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1ff8-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="b1ff8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ff8-122">CommonParameters</span></span>
<span data-ttu-id="b1ff8-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ff8-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1ff8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ff8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b1ff8-125">INPUTS</span></span>

### <span data-ttu-id="b1ff8-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1ff8-126">PSVirtualMachine</span></span>
<span data-ttu-id="b1ff8-127">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="b1ff8-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="b1ff8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b1ff8-128">OUTPUTS</span></span>

### <span data-ttu-id="b1ff8-129">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b1ff8-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1ff8-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b1ff8-130">NOTES</span></span>

## <span data-ttu-id="b1ff8-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1ff8-131">RELATED LINKS</span></span>

[<span data-ttu-id="b1ff8-132">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1ff8-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


