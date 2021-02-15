---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131239"
---
# <span data-ttu-id="b944a-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="b944a-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="b944a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b944a-102">SYNOPSIS</span></span>
<span data-ttu-id="b944a-103">建立新的 IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="b944a-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="b944a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b944a-104">SYNTAX</span></span>

### <span data-ttu-id="b944a-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b944a-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="b944a-106">說明</span><span class="sxs-lookup"><span data-stu-id="b944a-106">DESCRIPTION</span></span>
<span data-ttu-id="b944a-107">**新的-AzIpConfigurationBgpPeeringAddressObject** 會建立 IpConfigurationBgpPeeringAddressObject 物件，在您的虛擬網路閘道 bgpsettings 中代表 BgpPeeringAddresses 屬性。</span><span class="sxs-lookup"><span data-stu-id="b944a-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="b944a-108">示例</span><span class="sxs-lookup"><span data-stu-id="b944a-108">EXAMPLES</span></span>

### <span data-ttu-id="b944a-109">1：建立 AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="b944a-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="b944a-110">上述將會建立 IpConfigurationBgpPeeringAddressObject。此新物件將會 gw1ipconfBgp1。</span><span class="sxs-lookup"><span data-stu-id="b944a-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="b944a-111">參數</span><span class="sxs-lookup"><span data-stu-id="b944a-111">PARAMETERS</span></span>

### <span data-ttu-id="b944a-112">-確認</span><span class="sxs-lookup"><span data-stu-id="b944a-112">-Confirm</span></span>
<span data-ttu-id="b944a-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b944a-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b944a-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="b944a-114">-CustomAddress</span></span>
<span data-ttu-id="b944a-115">BgpPeeringAddresses 的虛擬網路閘道 CustomAddress 清單。</span><span class="sxs-lookup"><span data-stu-id="b944a-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="b944a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b944a-116">-DefaultProfile</span></span>
<span data-ttu-id="b944a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b944a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b944a-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b944a-118">-IpConfigurationId</span></span>
<span data-ttu-id="b944a-119">BgpPeeringAddresses 的虛擬網路閘道 IpConfigurationId。</span><span class="sxs-lookup"><span data-stu-id="b944a-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="b944a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b944a-120">-WhatIf</span></span>
<span data-ttu-id="b944a-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b944a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b944a-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b944a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b944a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b944a-123">CommonParameters</span></span>
<span data-ttu-id="b944a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b944a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b944a-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b944a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b944a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b944a-126">INPUTS</span></span>

### <span data-ttu-id="b944a-127">所有</span><span class="sxs-lookup"><span data-stu-id="b944a-127">None</span></span>

## <span data-ttu-id="b944a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b944a-128">OUTPUTS</span></span>

### <span data-ttu-id="b944a-129">PSIpConfigurationBgpPeeringAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b944a-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="b944a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b944a-130">NOTES</span></span>

## <span data-ttu-id="b944a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b944a-131">RELATED LINKS</span></span>
