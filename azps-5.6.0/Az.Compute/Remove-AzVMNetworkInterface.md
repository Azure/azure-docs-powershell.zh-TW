---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 247a066da4d6a8a84587e451850954df40ba7be4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916217"
---
# <span data-ttu-id="65fe6-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="65fe6-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="65fe6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="65fe6-103">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="65fe6-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="65fe6-104">語法</span><span class="sxs-lookup"><span data-stu-id="65fe6-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65fe6-105">描述</span><span class="sxs-lookup"><span data-stu-id="65fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="65fe6-106">**Remove-Az VIRTUALNetworkInterface** Cmdlet 會從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="65fe6-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="65fe6-107">例子</span><span class="sxs-lookup"><span data-stu-id="65fe6-107">EXAMPLES</span></span>

## <span data-ttu-id="65fe6-108">參數</span><span class="sxs-lookup"><span data-stu-id="65fe6-108">PARAMETERS</span></span>

### <span data-ttu-id="65fe6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fe6-109">-DefaultProfile</span></span>
<span data-ttu-id="65fe6-110">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="65fe6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65fe6-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="65fe6-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="65fe6-112">指定此 Cmdlet 移除的網路介面 ID 陣列。</span><span class="sxs-lookup"><span data-stu-id="65fe6-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-113">-VM</span><span class="sxs-lookup"><span data-stu-id="65fe6-113">-VM</span></span>
<span data-ttu-id="65fe6-114">指定此 Cmdlet 會移除網路介面的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="65fe6-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="65fe6-115">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65fe6-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-116">-確認</span><span class="sxs-lookup"><span data-stu-id="65fe6-116">-Confirm</span></span>
<span data-ttu-id="65fe6-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="65fe6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fe6-118">-WhatIf</span></span>
<span data-ttu-id="65fe6-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65fe6-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65fe6-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65fe6-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fe6-121">CommonParameters</span></span>
<span data-ttu-id="65fe6-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65fe6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fe6-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65fe6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fe6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="65fe6-124">INPUTS</span></span>

### <span data-ttu-id="65fe6-125">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="65fe6-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="65fe6-126">輸出</span><span class="sxs-lookup"><span data-stu-id="65fe6-126">OUTPUTS</span></span>

### <span data-ttu-id="65fe6-127">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="65fe6-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="65fe6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="65fe6-128">NOTES</span></span>

## <span data-ttu-id="65fe6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="65fe6-129">RELATED LINKS</span></span>

[<span data-ttu-id="65fe6-130">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="65fe6-130">Get-AzVM</span></span>](./Get-AzVM.md)


