---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: d8ef4378ed0032012a64d015855ca0287d608a6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911465"
---
# <span data-ttu-id="d884e-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d884e-101">New-AzPeering</span></span>

## <span data-ttu-id="d884e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d884e-102">SYNOPSIS</span></span>
<span data-ttu-id="d884e-103">建立新的對等 ARM 資源</span><span class="sxs-lookup"><span data-stu-id="d884e-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="d884e-104">語法</span><span class="sxs-lookup"><span data-stu-id="d884e-104">SYNTAX</span></span>

### <span data-ttu-id="d884e-105">Exchange (預設) </span><span class="sxs-lookup"><span data-stu-id="d884e-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d884e-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="d884e-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d884e-107">直接</span><span class="sxs-lookup"><span data-stu-id="d884e-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d884e-108">描述</span><span class="sxs-lookup"><span data-stu-id="d884e-108">DESCRIPTION</span></span>
<span data-ttu-id="d884e-109">為訂閱建立 ARM 對等。</span><span class="sxs-lookup"><span data-stu-id="d884e-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="d884e-110">請參閱 [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) 或 [New-AzPeeringExchangeConnectionObject，](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) 以瞭解有關建立連線物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="d884e-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="d884e-111">例子</span><span class="sxs-lookup"><span data-stu-id="d884e-111">EXAMPLES</span></span>

### <span data-ttu-id="d884e-112">建立新直接對等</span><span class="sxs-lookup"><span data-stu-id="d884e-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="d884e-113">使用 PeerAsn 65000 在西雅圖工廠建立單一連接的新直接對等</span><span class="sxs-lookup"><span data-stu-id="d884e-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="d884e-114">建立新的 Exchange 對等</span><span class="sxs-lookup"><span data-stu-id="d884e-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="d884e-115">建立新 Exchange 對等</span><span class="sxs-lookup"><span data-stu-id="d884e-115">Create a new exchange peering</span></span>

### <span data-ttu-id="d884e-116">將舊版對等轉換為 ARM 對等</span><span class="sxs-lookup"><span data-stu-id="d884e-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="d884e-117">參數</span><span class="sxs-lookup"><span data-stu-id="d884e-117">PARAMETERS</span></span>

### <span data-ttu-id="d884e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d884e-118">-AsJob</span></span>
<span data-ttu-id="d884e-119">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="d884e-119">Run in the background.</span></span>

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

### <span data-ttu-id="d884e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d884e-120">-DefaultProfile</span></span>
<span data-ttu-id="d884e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d884e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d884e-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="d884e-122">-DirectConnection</span></span>
<span data-ttu-id="d884e-123">使用命令的管道和New-AzExchangePeeringConnection來建立新的直接連接。</span><span class="sxs-lookup"><span data-stu-id="d884e-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="d884e-124">-ExchangeConnection</span></span>
<span data-ttu-id="d884e-125">使用這個命令的New-AzExchangePeeringConnection和管道來建立新的 Exchange 連結。</span><span class="sxs-lookup"><span data-stu-id="d884e-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d884e-126">-InputObject</span></span>
<span data-ttu-id="d884e-127">使用Get-AzLegacyPeering來取回此物件。</span><span class="sxs-lookup"><span data-stu-id="d884e-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="d884e-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="d884e-129">選取您想要對等的 Microsoft 網路。</span><span class="sxs-lookup"><span data-stu-id="d884e-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="d884e-130">-Name</span></span>
<span data-ttu-id="d884e-131">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d884e-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="d884e-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="d884e-133">對等 Asn 資源識別碼。Get-AzPeerAsn來取回識別碼。</span><span class="sxs-lookup"><span data-stu-id="d884e-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-134">-對等位置</span><span class="sxs-lookup"><span data-stu-id="d884e-134">-PeeringLocation</span></span>
<span data-ttu-id="d884e-135">與 Azure 區域不同的實體位置。</span><span class="sxs-lookup"><span data-stu-id="d884e-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="d884e-136">使用 Get-AzPeeringLocation \<kind\> -Kind 使用城市名稱做為金鑰。</span><span class="sxs-lookup"><span data-stu-id="d884e-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d884e-137">-ResourceGroupName</span></span>
<span data-ttu-id="d884e-138">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d884e-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="d884e-139">-Sku</span></span>
<span data-ttu-id="d884e-140">選取Basic_Direct_Free或Premium_Direct_Free，除非明確要求選取另一個選項。</span><span class="sxs-lookup"><span data-stu-id="d884e-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-141">-標記</span><span class="sxs-lookup"><span data-stu-id="d884e-141">-Tag</span></span>
<span data-ttu-id="d884e-142">要與 Microsoft 對等服務建立關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="d884e-142">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d884e-143">-確認</span><span class="sxs-lookup"><span data-stu-id="d884e-143">-Confirm</span></span>
<span data-ttu-id="d884e-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d884e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d884e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d884e-145">-WhatIf</span></span>
<span data-ttu-id="d884e-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d884e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d884e-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d884e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d884e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d884e-148">CommonParameters</span></span>
<span data-ttu-id="d884e-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d884e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d884e-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d884e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d884e-151">輸入</span><span class="sxs-lookup"><span data-stu-id="d884e-151">INPUTS</span></span>

### <span data-ttu-id="d884e-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="d884e-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="d884e-153">輸出</span><span class="sxs-lookup"><span data-stu-id="d884e-153">OUTPUTS</span></span>

### <span data-ttu-id="d884e-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="d884e-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="d884e-155">筆記</span><span class="sxs-lookup"><span data-stu-id="d884e-155">NOTES</span></span>

## <span data-ttu-id="d884e-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="d884e-156">RELATED LINKS</span></span>
