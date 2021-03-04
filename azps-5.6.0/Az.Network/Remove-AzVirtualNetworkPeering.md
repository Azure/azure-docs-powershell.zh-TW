---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912630"
---
# <span data-ttu-id="d14e5-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d14e5-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="d14e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d14e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d14e5-103">移除虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="d14e5-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="d14e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="d14e5-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d14e5-105">描述</span><span class="sxs-lookup"><span data-stu-id="d14e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d14e5-106">移除虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="d14e5-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="d14e5-107">例子</span><span class="sxs-lookup"><span data-stu-id="d14e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d14e5-108">範例 1：移除虛擬網路對等</span><span class="sxs-lookup"><span data-stu-id="d14e5-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d14e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="d14e5-109">PARAMETERS</span></span>

### <span data-ttu-id="d14e5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d14e5-110">-AsJob</span></span>
<span data-ttu-id="d14e5-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d14e5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d14e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14e5-112">-DefaultProfile</span></span>
<span data-ttu-id="d14e5-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d14e5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d14e5-114">-強制</span><span class="sxs-lookup"><span data-stu-id="d14e5-114">-Force</span></span>
<span data-ttu-id="d14e5-115">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d14e5-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d14e5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d14e5-116">-Name</span></span>
<span data-ttu-id="d14e5-117">虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="d14e5-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="d14e5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d14e5-118">-PassThru</span></span>
<span data-ttu-id="d14e5-119">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d14e5-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d14e5-120">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d14e5-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d14e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d14e5-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="d14e5-122">The resource group name</span></span>

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

### <span data-ttu-id="d14e5-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d14e5-123">-VirtualNetworkName</span></span>
<span data-ttu-id="d14e5-124">虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="d14e5-124">The virtual network name.</span></span>

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

### <span data-ttu-id="d14e5-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d14e5-125">-Confirm</span></span>
<span data-ttu-id="d14e5-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d14e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d14e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d14e5-127">-WhatIf</span></span>
<span data-ttu-id="d14e5-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d14e5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d14e5-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d14e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d14e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14e5-130">CommonParameters</span></span>
<span data-ttu-id="d14e5-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d14e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14e5-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d14e5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14e5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d14e5-133">INPUTS</span></span>

### <span data-ttu-id="d14e5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d14e5-134">System.String</span></span>

## <span data-ttu-id="d14e5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d14e5-135">OUTPUTS</span></span>

### <span data-ttu-id="d14e5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d14e5-136">System.Boolean</span></span>

## <span data-ttu-id="d14e5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d14e5-137">NOTES</span></span>

## <span data-ttu-id="d14e5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d14e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="d14e5-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d14e5-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d14e5-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d14e5-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d14e5-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d14e5-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
