---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: b77d741c0313e202304be3fd51fb3e1cd5b25b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445063"
---
# <span data-ttu-id="8939d-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8939d-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="8939d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8939d-102">SYNOPSIS</span></span>
<span data-ttu-id="8939d-103">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="8939d-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8939d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8939d-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8939d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8939d-105">DESCRIPTION</span></span>
<span data-ttu-id="8939d-106">**AzureRmVMNetworkInterface** Cmdlet 會將網路介面從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="8939d-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="8939d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8939d-107">EXAMPLES</span></span>

## <span data-ttu-id="8939d-108">參數</span><span class="sxs-lookup"><span data-stu-id="8939d-108">PARAMETERS</span></span>

### <span data-ttu-id="8939d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8939d-109">-DefaultProfile</span></span>
<span data-ttu-id="8939d-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8939d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8939d-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="8939d-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="8939d-112">指定此 Cmdlet 移除的網路介面 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="8939d-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8939d-113">-VM</span><span class="sxs-lookup"><span data-stu-id="8939d-113">-VM</span></span>
<span data-ttu-id="8939d-114">指定此 Cmdlet 移除網路介面的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8939d-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="8939d-115">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8939d-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="8939d-116">-確認</span><span class="sxs-lookup"><span data-stu-id="8939d-116">-Confirm</span></span>
<span data-ttu-id="8939d-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8939d-117">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="8939d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8939d-118">-WhatIf</span></span>
<span data-ttu-id="8939d-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8939d-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8939d-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8939d-120">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="8939d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8939d-121">CommonParameters</span></span>
<span data-ttu-id="8939d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8939d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8939d-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8939d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8939d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8939d-124">INPUTS</span></span>

## <span data-ttu-id="8939d-125">輸出</span><span class="sxs-lookup"><span data-stu-id="8939d-125">OUTPUTS</span></span>

## <span data-ttu-id="8939d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8939d-126">NOTES</span></span>

## <span data-ttu-id="8939d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8939d-127">RELATED LINKS</span></span>

[<span data-ttu-id="8939d-128">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8939d-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


