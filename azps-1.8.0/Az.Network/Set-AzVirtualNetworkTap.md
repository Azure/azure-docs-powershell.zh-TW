---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 5a68c17f26109f5000e82d31e21e0f0330b7c87a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621394"
---
# <span data-ttu-id="fa12d-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fa12d-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="fa12d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa12d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa12d-103">更新虛擬網路分流。</span><span class="sxs-lookup"><span data-stu-id="fa12d-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="fa12d-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa12d-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa12d-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa12d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa12d-106">**AzVirtualNetworkTap** Cmdlet 會更新虛擬網路分流。</span><span class="sxs-lookup"><span data-stu-id="fa12d-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="fa12d-107">示例</span><span class="sxs-lookup"><span data-stu-id="fa12d-107">EXAMPLES</span></span>

### <span data-ttu-id="fa12d-108">範例1：設定虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="fa12d-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="fa12d-109">此命令會更新目的地 IpConfiguration，並更新虛擬網路路器。</span><span class="sxs-lookup"><span data-stu-id="fa12d-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="fa12d-110">如果有任何的攻絲配置引用它，則所有來源流量都不會啟動，因此無法在新的目的地 ip 配置更新後進行鏡像。</span><span class="sxs-lookup"><span data-stu-id="fa12d-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="fa12d-111">參數</span><span class="sxs-lookup"><span data-stu-id="fa12d-111">PARAMETERS</span></span>

### <span data-ttu-id="fa12d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa12d-112">-AsJob</span></span>
<span data-ttu-id="fa12d-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa12d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa12d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa12d-114">-DefaultProfile</span></span>
<span data-ttu-id="fa12d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa12d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa12d-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fa12d-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="fa12d-117">虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="fa12d-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa12d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="fa12d-118">-Confirm</span></span>
<span data-ttu-id="fa12d-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa12d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa12d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa12d-120">-WhatIf</span></span>
<span data-ttu-id="fa12d-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa12d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa12d-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa12d-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa12d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa12d-123">CommonParameters</span></span>
<span data-ttu-id="fa12d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa12d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa12d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa12d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa12d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fa12d-126">INPUTS</span></span>

### <span data-ttu-id="fa12d-127">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fa12d-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="fa12d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fa12d-128">OUTPUTS</span></span>

### <span data-ttu-id="fa12d-129">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fa12d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="fa12d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fa12d-130">NOTES</span></span>

## <span data-ttu-id="fa12d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa12d-131">RELATED LINKS</span></span>

[<span data-ttu-id="fa12d-132">AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fa12d-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="fa12d-133">新-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fa12d-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="fa12d-134">移除-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fa12d-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
