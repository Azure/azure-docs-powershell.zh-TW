---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128359"
---
# <span data-ttu-id="7278f-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7278f-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="7278f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7278f-102">SYNOPSIS</span></span>
<span data-ttu-id="7278f-103">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="7278f-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="7278f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7278f-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7278f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7278f-105">DESCRIPTION</span></span>
<span data-ttu-id="7278f-106">**AzVMNetworkInterface** Cmdlet 會將網路介面從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="7278f-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="7278f-107">示例</span><span class="sxs-lookup"><span data-stu-id="7278f-107">EXAMPLES</span></span>

## <span data-ttu-id="7278f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7278f-108">PARAMETERS</span></span>

### <span data-ttu-id="7278f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7278f-109">-DefaultProfile</span></span>
<span data-ttu-id="7278f-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7278f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7278f-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="7278f-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="7278f-112">指定此 Cmdlet 移除的網路介面 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="7278f-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7278f-113">-VM</span><span class="sxs-lookup"><span data-stu-id="7278f-113">-VM</span></span>
<span data-ttu-id="7278f-114">指定此 Cmdlet 移除網路介面的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7278f-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="7278f-115">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7278f-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="7278f-116">-確認</span><span class="sxs-lookup"><span data-stu-id="7278f-116">-Confirm</span></span>
<span data-ttu-id="7278f-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7278f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7278f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7278f-118">-WhatIf</span></span>
<span data-ttu-id="7278f-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7278f-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7278f-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7278f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7278f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7278f-121">CommonParameters</span></span>
<span data-ttu-id="7278f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7278f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7278f-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7278f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7278f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7278f-124">INPUTS</span></span>

### <span data-ttu-id="7278f-125">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7278f-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7278f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7278f-126">OUTPUTS</span></span>

### <span data-ttu-id="7278f-127">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7278f-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7278f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7278f-128">NOTES</span></span>

## <span data-ttu-id="7278f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7278f-129">RELATED LINKS</span></span>

[<span data-ttu-id="7278f-130">AzVM</span><span class="sxs-lookup"><span data-stu-id="7278f-130">Get-AzVM</span></span>](./Get-AzVM.md)

