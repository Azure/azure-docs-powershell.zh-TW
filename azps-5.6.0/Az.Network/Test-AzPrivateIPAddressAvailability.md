---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: a39dd390e0307662c8105bf84999ae8dfc1fc7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901853"
---
# <span data-ttu-id="c1034-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="c1034-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="c1034-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1034-102">SYNOPSIS</span></span>
<span data-ttu-id="c1034-103">測試虛擬網路中私人 IP 位址的可用性。</span><span class="sxs-lookup"><span data-stu-id="c1034-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="c1034-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1034-104">SYNTAX</span></span>

### <span data-ttu-id="c1034-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="c1034-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1034-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1034-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1034-107">描述</span><span class="sxs-lookup"><span data-stu-id="c1034-107">DESCRIPTION</span></span>
<span data-ttu-id="c1034-108">**Test-AzPrivateIPAddressAvailability** Cmdlet 會測試指定的私人 IP 位址是否可以在虛擬網路中使用。</span><span class="sxs-lookup"><span data-stu-id="c1034-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="c1034-109">如果已取用要求的私人 IP 位址，此 Cmdlet 會返回可用的私人 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="c1034-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="c1034-110">例子</span><span class="sxs-lookup"><span data-stu-id="c1034-110">EXAMPLES</span></span>

### <span data-ttu-id="c1034-111">範例 1：測試是否使用管線提供 IP 位址</span><span class="sxs-lookup"><span data-stu-id="c1034-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="c1034-112">此命令會獲得一個虛擬網路，並使用管線運算子將它傳遞到 **Test-AzPrivateIPAddressAvailability，** 這會測試指定的私人 IP 位址是否可用。</span><span class="sxs-lookup"><span data-stu-id="c1034-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="c1034-113">參數</span><span class="sxs-lookup"><span data-stu-id="c1034-113">PARAMETERS</span></span>

### <span data-ttu-id="c1034-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1034-114">-DefaultProfile</span></span>
<span data-ttu-id="c1034-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1034-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1034-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="c1034-116">-IPAddress</span></span>
<span data-ttu-id="c1034-117">指定要測試的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1034-117">Specifies the IP address to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1034-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1034-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1034-119">指定虛擬網路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c1034-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1034-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c1034-120">-VirtualNetwork</span></span>
<span data-ttu-id="c1034-121">指定 **PSVirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="c1034-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1034-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c1034-122">-VirtualNetworkName</span></span>
<span data-ttu-id="c1034-123">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1034-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1034-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1034-124">CommonParameters</span></span>
<span data-ttu-id="c1034-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1034-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1034-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c1034-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1034-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c1034-127">INPUTS</span></span>

### <span data-ttu-id="c1034-128">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c1034-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c1034-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c1034-129">OUTPUTS</span></span>

### <span data-ttu-id="c1034-130">Microsoft.Azure.Commands.Network.models.PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="c1034-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="c1034-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c1034-131">NOTES</span></span>

## <span data-ttu-id="c1034-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1034-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1034-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c1034-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


