---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 22d2396e4471e2321ff9e532d4361909baa67163
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901926"
---
# <span data-ttu-id="90dee-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="90dee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90dee-102">SYNOPSIS</span></span>
<span data-ttu-id="90dee-103">更新虛擬網路點一下。</span><span class="sxs-lookup"><span data-stu-id="90dee-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="90dee-104">語法</span><span class="sxs-lookup"><span data-stu-id="90dee-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90dee-105">描述</span><span class="sxs-lookup"><span data-stu-id="90dee-105">DESCRIPTION</span></span>
<span data-ttu-id="90dee-106">**Set-AzVirtualNetworkTap** Cmdlet 會更新虛擬網路點一下。</span><span class="sxs-lookup"><span data-stu-id="90dee-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="90dee-107">例子</span><span class="sxs-lookup"><span data-stu-id="90dee-107">EXAMPLES</span></span>

### <span data-ttu-id="90dee-108">範例 1：設定虛擬網路點兩下</span><span class="sxs-lookup"><span data-stu-id="90dee-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="90dee-109">命令會更新目的地 IpConfiguration，並更新虛擬網路點一下。</span><span class="sxs-lookup"><span data-stu-id="90dee-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="90dee-110">如果有任一點組配置參照，則更新後，所有來源流量不會開始鏡像到新的目的地 ip 組配置。</span><span class="sxs-lookup"><span data-stu-id="90dee-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="90dee-111">參數</span><span class="sxs-lookup"><span data-stu-id="90dee-111">PARAMETERS</span></span>

### <span data-ttu-id="90dee-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90dee-112">-AsJob</span></span>
<span data-ttu-id="90dee-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="90dee-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90dee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dee-114">-DefaultProfile</span></span>
<span data-ttu-id="90dee-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90dee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90dee-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="90dee-117">虛擬網路點一下</span><span class="sxs-lookup"><span data-stu-id="90dee-117">The virtual network tap</span></span>

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

### <span data-ttu-id="90dee-118">-確認</span><span class="sxs-lookup"><span data-stu-id="90dee-118">-Confirm</span></span>
<span data-ttu-id="90dee-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90dee-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90dee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90dee-120">-WhatIf</span></span>
<span data-ttu-id="90dee-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90dee-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90dee-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90dee-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90dee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dee-123">CommonParameters</span></span>
<span data-ttu-id="90dee-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90dee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dee-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="90dee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dee-126">輸入</span><span class="sxs-lookup"><span data-stu-id="90dee-126">INPUTS</span></span>

### <span data-ttu-id="90dee-127">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="90dee-128">輸出</span><span class="sxs-lookup"><span data-stu-id="90dee-128">OUTPUTS</span></span>

### <span data-ttu-id="90dee-129">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="90dee-130">筆記</span><span class="sxs-lookup"><span data-stu-id="90dee-130">NOTES</span></span>

## <span data-ttu-id="90dee-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="90dee-131">RELATED LINKS</span></span>

[<span data-ttu-id="90dee-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="90dee-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="90dee-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="90dee-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
