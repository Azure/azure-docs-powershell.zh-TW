---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 44a7dd8c0fbb3193ac514f9c1b447394b29574f3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400054"
---
# <span data-ttu-id="1772d-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1772d-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="1772d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1772d-102">SYNOPSIS</span></span>
<span data-ttu-id="1772d-103">移除 ExpressRoute 交叉連接對等互連組。</span><span class="sxs-lookup"><span data-stu-id="1772d-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="1772d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1772d-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1772d-105">描述</span><span class="sxs-lookup"><span data-stu-id="1772d-105">DESCRIPTION</span></span>
<span data-ttu-id="1772d-106">**Remove-AzExpressRouteCrossConnectionPeering** Cmdlet 會移除 ExpressRoute 交叉連接對等組。</span><span class="sxs-lookup"><span data-stu-id="1772d-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="1772d-107">例子</span><span class="sxs-lookup"><span data-stu-id="1772d-107">EXAMPLES</span></span>

### <span data-ttu-id="1772d-108">範例 1：從 ExpressRoute 交叉連接移除對等組</span><span class="sxs-lookup"><span data-stu-id="1772d-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="1772d-109">參數</span><span class="sxs-lookup"><span data-stu-id="1772d-109">PARAMETERS</span></span>

### <span data-ttu-id="1772d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1772d-110">-DefaultProfile</span></span>
<span data-ttu-id="1772d-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1772d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1772d-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1772d-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1772d-113">包含要移除對等配置的 ExpressRoute 交叉連接。</span><span class="sxs-lookup"><span data-stu-id="1772d-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="1772d-114">-強制</span><span class="sxs-lookup"><span data-stu-id="1772d-114">-Force</span></span>
<span data-ttu-id="1772d-115">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="1772d-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1772d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1772d-116">-Name</span></span>
<span data-ttu-id="1772d-117">要移除的對等組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1772d-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="1772d-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1772d-118">-PeerAddressType</span></span>
<span data-ttu-id="1772d-119">對等的網址系列</span><span class="sxs-lookup"><span data-stu-id="1772d-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="1772d-120">-確認</span><span class="sxs-lookup"><span data-stu-id="1772d-120">-Confirm</span></span>
<span data-ttu-id="1772d-121">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1772d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1772d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1772d-122">-WhatIf</span></span>
<span data-ttu-id="1772d-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1772d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1772d-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1772d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1772d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1772d-125">CommonParameters</span></span>
<span data-ttu-id="1772d-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1772d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1772d-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1772d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1772d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1772d-128">INPUTS</span></span>

### <span data-ttu-id="1772d-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1772d-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="1772d-130">參數 'ExpressRouteCrossConnection' 接受來自管線之類型 'PSExpressRouteCrossConnection'的值</span><span class="sxs-lookup"><span data-stu-id="1772d-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="1772d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1772d-131">OUTPUTS</span></span>

### <span data-ttu-id="1772d-132">Microsoft.Azure.Commands.Network.models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1772d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1772d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1772d-133">NOTES</span></span>

## <span data-ttu-id="1772d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1772d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1772d-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1772d-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)



[<span data-ttu-id="1772d-136">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1772d-136">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="1772d-137">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1772d-137">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
