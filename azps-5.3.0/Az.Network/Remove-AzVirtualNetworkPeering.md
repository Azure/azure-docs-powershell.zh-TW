---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450171"
---
# <span data-ttu-id="4fe37-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4fe37-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="4fe37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fe37-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe37-103">移除虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="4fe37-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="4fe37-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fe37-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe37-105">說明</span><span class="sxs-lookup"><span data-stu-id="4fe37-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe37-106">移除虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="4fe37-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="4fe37-107">示例</span><span class="sxs-lookup"><span data-stu-id="4fe37-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe37-108">範例1：移除虛擬網路對等</span><span class="sxs-lookup"><span data-stu-id="4fe37-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="4fe37-109">參數</span><span class="sxs-lookup"><span data-stu-id="4fe37-109">PARAMETERS</span></span>

### <span data-ttu-id="4fe37-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fe37-110">-AsJob</span></span>
<span data-ttu-id="4fe37-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4fe37-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fe37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe37-112">-DefaultProfile</span></span>
<span data-ttu-id="4fe37-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fe37-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fe37-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4fe37-114">-Force</span></span>
<span data-ttu-id="4fe37-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4fe37-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fe37-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fe37-116">-Name</span></span>
<span data-ttu-id="4fe37-117">虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe37-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="4fe37-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fe37-118">-PassThru</span></span>
<span data-ttu-id="4fe37-119">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4fe37-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4fe37-120">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4fe37-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4fe37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe37-121">-ResourceGroupName</span></span>
<span data-ttu-id="4fe37-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4fe37-122">The resource group name</span></span>

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

### <span data-ttu-id="4fe37-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4fe37-123">-VirtualNetworkName</span></span>
<span data-ttu-id="4fe37-124">虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe37-124">The virtual network name.</span></span>

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

### <span data-ttu-id="4fe37-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4fe37-125">-Confirm</span></span>
<span data-ttu-id="4fe37-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4fe37-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe37-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe37-127">-WhatIf</span></span>
<span data-ttu-id="4fe37-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fe37-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fe37-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fe37-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe37-130">CommonParameters</span></span>
<span data-ttu-id="4fe37-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fe37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe37-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fe37-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe37-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4fe37-133">INPUTS</span></span>

### <span data-ttu-id="4fe37-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4fe37-134">System.String</span></span>

## <span data-ttu-id="4fe37-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4fe37-135">OUTPUTS</span></span>

### <span data-ttu-id="4fe37-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4fe37-136">System.Boolean</span></span>

## <span data-ttu-id="4fe37-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4fe37-137">NOTES</span></span>

## <span data-ttu-id="4fe37-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fe37-138">RELATED LINKS</span></span>

[<span data-ttu-id="4fe37-139">附加 AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4fe37-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="4fe37-140">AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4fe37-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="4fe37-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4fe37-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
