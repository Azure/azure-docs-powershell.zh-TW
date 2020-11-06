---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b991b26d8d6fc7a7cfd33ab051619b7192ae0aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621621"
---
# <span data-ttu-id="80284-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="80284-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="80284-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80284-102">SYNOPSIS</span></span>
<span data-ttu-id="80284-103">移除 ExpressRoute 交叉連接對等設定。</span><span class="sxs-lookup"><span data-stu-id="80284-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="80284-104">句法</span><span class="sxs-lookup"><span data-stu-id="80284-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80284-105">說明</span><span class="sxs-lookup"><span data-stu-id="80284-105">DESCRIPTION</span></span>
<span data-ttu-id="80284-106">**AzExpressRouteCrossConnectionPeering** Cmdlet 會移除 ExpressRoute 交叉連接對等設定。</span><span class="sxs-lookup"><span data-stu-id="80284-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="80284-107">示例</span><span class="sxs-lookup"><span data-stu-id="80284-107">EXAMPLES</span></span>

### <span data-ttu-id="80284-108">範例1：從 ExpressRoute 交叉連線中移除對等設定</span><span class="sxs-lookup"><span data-stu-id="80284-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="80284-109">參數</span><span class="sxs-lookup"><span data-stu-id="80284-109">PARAMETERS</span></span>

### <span data-ttu-id="80284-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80284-110">-DefaultProfile</span></span>
<span data-ttu-id="80284-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80284-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80284-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="80284-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="80284-113">包含要移除之對等設定的 ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="80284-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80284-114">-Force</span><span class="sxs-lookup"><span data-stu-id="80284-114">-Force</span></span>
<span data-ttu-id="80284-115">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="80284-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="80284-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="80284-116">-Name</span></span>
<span data-ttu-id="80284-117">要移除之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="80284-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80284-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="80284-118">-PeerAddressType</span></span>
<span data-ttu-id="80284-119">對等的位址族</span><span class="sxs-lookup"><span data-stu-id="80284-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80284-120">-確認</span><span class="sxs-lookup"><span data-stu-id="80284-120">-Confirm</span></span>
<span data-ttu-id="80284-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80284-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80284-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80284-122">-WhatIf</span></span>
<span data-ttu-id="80284-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80284-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80284-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80284-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80284-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80284-125">CommonParameters</span></span>
<span data-ttu-id="80284-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80284-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80284-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80284-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80284-128">輸入</span><span class="sxs-lookup"><span data-stu-id="80284-128">INPUTS</span></span>

### <span data-ttu-id="80284-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="80284-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="80284-130">形參 "ExpressRouteCrossConnection" 接受管線中 "PSExpressRouteCrossConnection" 類型的值</span><span class="sxs-lookup"><span data-stu-id="80284-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="80284-131">輸出</span><span class="sxs-lookup"><span data-stu-id="80284-131">OUTPUTS</span></span>

### <span data-ttu-id="80284-132">PSExpressRouteCrossConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80284-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="80284-133">筆記</span><span class="sxs-lookup"><span data-stu-id="80284-133">NOTES</span></span>

## <span data-ttu-id="80284-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="80284-134">RELATED LINKS</span></span>

[<span data-ttu-id="80284-135">附加 AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="80284-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="80284-136">AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="80284-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="80284-137">AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="80284-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="80284-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="80284-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
