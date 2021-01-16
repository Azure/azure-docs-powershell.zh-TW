---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288456"
---
# <span data-ttu-id="e98da-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e98da-101">Update-AzPeering</span></span>

## <span data-ttu-id="e98da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e98da-102">SYNOPSIS</span></span>
<span data-ttu-id="e98da-103">設定對等。</span><span class="sxs-lookup"><span data-stu-id="e98da-103">Sets the Peering.</span></span> <span data-ttu-id="e98da-104">將此命令與 or 搭配 `Set-AzDirectPeeringConnectionObject` 使用 `Set-AzExchangePeeringConnectionObject` 。</span><span class="sxs-lookup"><span data-stu-id="e98da-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="e98da-105">句法</span><span class="sxs-lookup"><span data-stu-id="e98da-105">SYNTAX</span></span>

### <span data-ttu-id="e98da-106">DefaultExchange (預設) </span><span class="sxs-lookup"><span data-stu-id="e98da-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98da-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="e98da-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98da-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="e98da-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98da-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="e98da-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98da-110">播放</span><span class="sxs-lookup"><span data-stu-id="e98da-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98da-111">證券</span><span class="sxs-lookup"><span data-stu-id="e98da-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e98da-112">說明</span><span class="sxs-lookup"><span data-stu-id="e98da-112">DESCRIPTION</span></span>
<span data-ttu-id="e98da-113">設定 PSPeering 物件</span><span class="sxs-lookup"><span data-stu-id="e98da-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="e98da-114">示例</span><span class="sxs-lookup"><span data-stu-id="e98da-114">EXAMPLES</span></span>

### <span data-ttu-id="e98da-115">更新 Md5 驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="e98da-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="e98da-116">設定 Md5 驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="e98da-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="e98da-117">更新 UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="e98da-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="e98da-118">設定對等服務標章的使用</span><span class="sxs-lookup"><span data-stu-id="e98da-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="e98da-119">更新 Exchange 對等的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="e98da-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="e98da-120">使用 ResourceId 設定 Exchange 對等的 Ipv4 位址</span><span class="sxs-lookup"><span data-stu-id="e98da-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="e98da-121">參數</span><span class="sxs-lookup"><span data-stu-id="e98da-121">PARAMETERS</span></span>

### <span data-ttu-id="e98da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98da-122">-DefaultProfile</span></span>
<span data-ttu-id="e98da-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e98da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98da-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="e98da-124">-DirectConnection</span></span>
<span data-ttu-id="e98da-125">使用 New-AzDirectPeeringConnectionObject 和 pipe 建立新的直接連線至此命令。</span><span class="sxs-lookup"><span data-stu-id="e98da-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="e98da-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e98da-126">-ExchangeConnection</span></span>
<span data-ttu-id="e98da-127">使用 New-AzExchangePeeringConnectionObject 和管道建立新的 Exchange 連線至此命令。</span><span class="sxs-lookup"><span data-stu-id="e98da-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="e98da-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e98da-128">-InputObject</span></span>
<span data-ttu-id="e98da-129">對等物件</span><span class="sxs-lookup"><span data-stu-id="e98da-129">The Peering object</span></span> 

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

### <span data-ttu-id="e98da-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="e98da-130">-Name</span></span>
<span data-ttu-id="e98da-131">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="e98da-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e98da-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e98da-132">-ResourceGroupName</span></span>
<span data-ttu-id="e98da-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e98da-133">The resource group name.</span></span>

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

### <span data-ttu-id="e98da-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e98da-134">-ResourceId</span></span>
<span data-ttu-id="e98da-135">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="e98da-135">The resource id string name.</span></span>

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

### <span data-ttu-id="e98da-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e98da-136">-Confirm</span></span>
<span data-ttu-id="e98da-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e98da-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e98da-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e98da-138">-WhatIf</span></span>
<span data-ttu-id="e98da-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e98da-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e98da-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e98da-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e98da-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98da-141">CommonParameters</span></span>
<span data-ttu-id="e98da-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e98da-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98da-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e98da-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98da-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e98da-144">INPUTS</span></span>

### <span data-ttu-id="e98da-145">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="e98da-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e98da-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e98da-146">System.String</span></span>

## <span data-ttu-id="e98da-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e98da-147">OUTPUTS</span></span>

### <span data-ttu-id="e98da-148">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="e98da-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e98da-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e98da-149">NOTES</span></span>

## <span data-ttu-id="e98da-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e98da-150">RELATED LINKS</span></span>
