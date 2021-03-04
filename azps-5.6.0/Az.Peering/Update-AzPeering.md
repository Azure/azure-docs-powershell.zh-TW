---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0824693c2d9f849b80f36065814f8dc57209a2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911390"
---
# <span data-ttu-id="06db5-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="06db5-101">Update-AzPeering</span></span>

## <span data-ttu-id="06db5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06db5-102">SYNOPSIS</span></span>
<span data-ttu-id="06db5-103">設定對等。</span><span class="sxs-lookup"><span data-stu-id="06db5-103">Sets the Peering.</span></span> <span data-ttu-id="06db5-104">將此命令與或 `Set-AzDirectPeeringConnectionObject` 同時使用 `Set-AzExchangePeeringConnectionObject` 。</span><span class="sxs-lookup"><span data-stu-id="06db5-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="06db5-105">語法</span><span class="sxs-lookup"><span data-stu-id="06db5-105">SYNTAX</span></span>

### <span data-ttu-id="06db5-106">DefaultExchange (預設) </span><span class="sxs-lookup"><span data-stu-id="06db5-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06db5-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="06db5-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06db5-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="06db5-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06db5-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="06db5-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06db5-110">直接</span><span class="sxs-lookup"><span data-stu-id="06db5-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06db5-111">交換</span><span class="sxs-lookup"><span data-stu-id="06db5-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06db5-112">描述</span><span class="sxs-lookup"><span data-stu-id="06db5-112">DESCRIPTION</span></span>
<span data-ttu-id="06db5-113">設定 PSPeering 物件</span><span class="sxs-lookup"><span data-stu-id="06db5-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="06db5-114">例子</span><span class="sxs-lookup"><span data-stu-id="06db5-114">EXAMPLES</span></span>

### <span data-ttu-id="06db5-115">更新 Md5 驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="06db5-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="06db5-116">設定 Md5 驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="06db5-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="06db5-117">更新 UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="06db5-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="06db5-118">設定對等服務使用標號</span><span class="sxs-lookup"><span data-stu-id="06db5-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="06db5-119">更新 Exchange 對等的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="06db5-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="06db5-120">使用 ResourceId 設定 Exchange 對等的 Ipv4 位址</span><span class="sxs-lookup"><span data-stu-id="06db5-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="06db5-121">參數</span><span class="sxs-lookup"><span data-stu-id="06db5-121">PARAMETERS</span></span>

### <span data-ttu-id="06db5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06db5-122">-DefaultProfile</span></span>
<span data-ttu-id="06db5-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06db5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06db5-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="06db5-124">-DirectConnection</span></span>
<span data-ttu-id="06db5-125">使用命令的管道和New-AzDirectPeeringConnectionObject來建立新的直接連接。</span><span class="sxs-lookup"><span data-stu-id="06db5-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06db5-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="06db5-126">-ExchangeConnection</span></span>
<span data-ttu-id="06db5-127">使用這個命令的New-AzExchangePeeringConnectionObject和管道來建立新的 Exchange 連接。</span><span class="sxs-lookup"><span data-stu-id="06db5-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06db5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06db5-128">-InputObject</span></span>
<span data-ttu-id="06db5-129">對等物件</span><span class="sxs-lookup"><span data-stu-id="06db5-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06db5-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="06db5-130">-Name</span></span>
<span data-ttu-id="06db5-131">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="06db5-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06db5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06db5-132">-ResourceGroupName</span></span>
<span data-ttu-id="06db5-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="06db5-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06db5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06db5-134">-ResourceId</span></span>
<span data-ttu-id="06db5-135">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="06db5-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06db5-136">-確認</span><span class="sxs-lookup"><span data-stu-id="06db5-136">-Confirm</span></span>
<span data-ttu-id="06db5-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06db5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06db5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06db5-138">-WhatIf</span></span>
<span data-ttu-id="06db5-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06db5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06db5-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06db5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06db5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06db5-141">CommonParameters</span></span>
<span data-ttu-id="06db5-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06db5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06db5-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06db5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06db5-144">輸入</span><span class="sxs-lookup"><span data-stu-id="06db5-144">INPUTS</span></span>

### <span data-ttu-id="06db5-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="06db5-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="06db5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="06db5-146">System.String</span></span>

## <span data-ttu-id="06db5-147">輸出</span><span class="sxs-lookup"><span data-stu-id="06db5-147">OUTPUTS</span></span>

### <span data-ttu-id="06db5-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="06db5-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="06db5-149">筆記</span><span class="sxs-lookup"><span data-stu-id="06db5-149">NOTES</span></span>

## <span data-ttu-id="06db5-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="06db5-150">RELATED LINKS</span></span>
