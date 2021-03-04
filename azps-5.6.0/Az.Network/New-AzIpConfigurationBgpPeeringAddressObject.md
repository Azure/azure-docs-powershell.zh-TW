---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: ba713650670abdeb9c64242109b30f47d99724f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914730"
---
# <span data-ttu-id="84d41-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="84d41-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="84d41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84d41-102">SYNOPSIS</span></span>
<span data-ttu-id="84d41-103">建立新 IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="84d41-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="84d41-104">語法</span><span class="sxs-lookup"><span data-stu-id="84d41-104">SYNTAX</span></span>

### <span data-ttu-id="84d41-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="84d41-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="84d41-106">描述</span><span class="sxs-lookup"><span data-stu-id="84d41-106">DESCRIPTION</span></span>
<span data-ttu-id="84d41-107">**New-AzIpConfigurationBgpPeeringAddressObject** 會建立 IpConfigurationBgpPeeringAddressObject 物件，代表您虛擬網路閘道 bgpsettings 中的 BgpPeeringAddresses 屬性。</span><span class="sxs-lookup"><span data-stu-id="84d41-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="84d41-108">例子</span><span class="sxs-lookup"><span data-stu-id="84d41-108">EXAMPLES</span></span>

### <span data-ttu-id="84d41-109">1：建立 AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="84d41-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="84d41-110">上述將會建立一個 IpConfigurationBgpPeeringAddressObject。這個新的物件將會是 gw1ipconfBgp1。</span><span class="sxs-lookup"><span data-stu-id="84d41-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="84d41-111">參數</span><span class="sxs-lookup"><span data-stu-id="84d41-111">PARAMETERS</span></span>

### <span data-ttu-id="84d41-112">-確認</span><span class="sxs-lookup"><span data-stu-id="84d41-112">-Confirm</span></span>
<span data-ttu-id="84d41-113">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84d41-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d41-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="84d41-114">-CustomAddress</span></span>
<span data-ttu-id="84d41-115">BgpPeeringAddresses 的虛擬網路閘道 CustomAddress 清單。</span><span class="sxs-lookup"><span data-stu-id="84d41-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d41-116">-DefaultProfile</span></span>
<span data-ttu-id="84d41-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84d41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d41-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="84d41-118">-IpConfigurationId</span></span>
<span data-ttu-id="84d41-119">適用于 BgpPeeringAddresses 的虛擬網路閘道 IpConfigurationId。</span><span class="sxs-lookup"><span data-stu-id="84d41-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d41-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d41-120">-WhatIf</span></span>
<span data-ttu-id="84d41-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84d41-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d41-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84d41-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d41-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d41-123">CommonParameters</span></span>
<span data-ttu-id="84d41-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84d41-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d41-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84d41-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d41-126">輸入</span><span class="sxs-lookup"><span data-stu-id="84d41-126">INPUTS</span></span>

### <span data-ttu-id="84d41-127">沒有</span><span class="sxs-lookup"><span data-stu-id="84d41-127">None</span></span>

## <span data-ttu-id="84d41-128">輸出</span><span class="sxs-lookup"><span data-stu-id="84d41-128">OUTPUTS</span></span>

### <span data-ttu-id="84d41-129">Microsoft.Azure.Commands.network.models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="84d41-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="84d41-130">筆記</span><span class="sxs-lookup"><span data-stu-id="84d41-130">NOTES</span></span>

## <span data-ttu-id="84d41-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="84d41-131">RELATED LINKS</span></span>
