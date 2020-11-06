---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3071b07e73d5038b5efef8a76b689dc0fff87e01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621546"
---
# <span data-ttu-id="79921-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="79921-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="79921-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79921-102">SYNOPSIS</span></span>
<span data-ttu-id="79921-103">移除虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="79921-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="79921-104">句法</span><span class="sxs-lookup"><span data-stu-id="79921-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79921-105">說明</span><span class="sxs-lookup"><span data-stu-id="79921-105">DESCRIPTION</span></span>
<span data-ttu-id="79921-106">移除虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="79921-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="79921-107">示例</span><span class="sxs-lookup"><span data-stu-id="79921-107">EXAMPLES</span></span>

### <span data-ttu-id="79921-108">範例1：移除虛擬網路對等</span><span class="sxs-lookup"><span data-stu-id="79921-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="79921-109">參數</span><span class="sxs-lookup"><span data-stu-id="79921-109">PARAMETERS</span></span>

### <span data-ttu-id="79921-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79921-110">-AsJob</span></span>
<span data-ttu-id="79921-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="79921-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79921-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79921-112">-DefaultProfile</span></span>
<span data-ttu-id="79921-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79921-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79921-114">-Force</span><span class="sxs-lookup"><span data-stu-id="79921-114">-Force</span></span>
<span data-ttu-id="79921-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="79921-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79921-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="79921-116">-Name</span></span>
<span data-ttu-id="79921-117">虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="79921-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79921-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79921-118">-PassThru</span></span>
<span data-ttu-id="79921-119">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="79921-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="79921-120">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="79921-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79921-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79921-121">-ResourceGroupName</span></span>
<span data-ttu-id="79921-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="79921-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79921-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="79921-123">-VirtualNetworkName</span></span>
<span data-ttu-id="79921-124">虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="79921-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79921-125">-確認</span><span class="sxs-lookup"><span data-stu-id="79921-125">-Confirm</span></span>
<span data-ttu-id="79921-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79921-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79921-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79921-127">-WhatIf</span></span>
<span data-ttu-id="79921-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79921-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79921-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79921-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79921-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79921-130">CommonParameters</span></span>
<span data-ttu-id="79921-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79921-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79921-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79921-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79921-133">輸入</span><span class="sxs-lookup"><span data-stu-id="79921-133">INPUTS</span></span>

### <span data-ttu-id="79921-134">System.object</span><span class="sxs-lookup"><span data-stu-id="79921-134">System.String</span></span>

## <span data-ttu-id="79921-135">輸出</span><span class="sxs-lookup"><span data-stu-id="79921-135">OUTPUTS</span></span>

### <span data-ttu-id="79921-136">System.object</span><span class="sxs-lookup"><span data-stu-id="79921-136">System.Boolean</span></span>

## <span data-ttu-id="79921-137">筆記</span><span class="sxs-lookup"><span data-stu-id="79921-137">NOTES</span></span>

## <span data-ttu-id="79921-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="79921-138">RELATED LINKS</span></span>

[<span data-ttu-id="79921-139">附加 AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="79921-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="79921-140">AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="79921-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="79921-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="79921-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
