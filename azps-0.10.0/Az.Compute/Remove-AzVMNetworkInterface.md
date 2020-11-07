---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796014"
---
# <span data-ttu-id="94f8b-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94f8b-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="94f8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="94f8b-103">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="94f8b-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="94f8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="94f8b-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f8b-105">說明</span><span class="sxs-lookup"><span data-stu-id="94f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="94f8b-106">**AzVMNetworkInterface** Cmdlet 會將網路介面從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="94f8b-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="94f8b-107">示例</span><span class="sxs-lookup"><span data-stu-id="94f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="94f8b-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="94f8b-108">1:</span></span>
```

```

## <span data-ttu-id="94f8b-109">參數</span><span class="sxs-lookup"><span data-stu-id="94f8b-109">PARAMETERS</span></span>

### <span data-ttu-id="94f8b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f8b-110">-DefaultProfile</span></span>
<span data-ttu-id="94f8b-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f8b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f8b-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="94f8b-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="94f8b-113">指定此 Cmdlet 移除的網路介面 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="94f8b-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94f8b-114">-VM</span><span class="sxs-lookup"><span data-stu-id="94f8b-114">-VM</span></span>
<span data-ttu-id="94f8b-115">指定此 Cmdlet 移除網路介面的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="94f8b-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="94f8b-116">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f8b-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="94f8b-117">-確認</span><span class="sxs-lookup"><span data-stu-id="94f8b-117">-Confirm</span></span>
<span data-ttu-id="94f8b-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94f8b-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="94f8b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f8b-119">-WhatIf</span></span>
<span data-ttu-id="94f8b-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94f8b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94f8b-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f8b-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="94f8b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f8b-122">CommonParameters</span></span>
<span data-ttu-id="94f8b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94f8b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f8b-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94f8b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f8b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="94f8b-125">INPUTS</span></span>

### <span data-ttu-id="94f8b-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="94f8b-126">PSVirtualMachine</span></span>
<span data-ttu-id="94f8b-127">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="94f8b-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="94f8b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="94f8b-128">OUTPUTS</span></span>

### <span data-ttu-id="94f8b-129">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="94f8b-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="94f8b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="94f8b-130">NOTES</span></span>

## <span data-ttu-id="94f8b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f8b-131">RELATED LINKS</span></span>

[<span data-ttu-id="94f8b-132">AzVM</span><span class="sxs-lookup"><span data-stu-id="94f8b-132">Get-AzVM</span></span>](./Get-AzVM.md)


