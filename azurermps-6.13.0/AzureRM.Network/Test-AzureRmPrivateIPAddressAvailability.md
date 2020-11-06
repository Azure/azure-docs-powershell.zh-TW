---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 2367f57db4e028710dce18acacd5b644b41f335b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450213"
---
# <span data-ttu-id="e02e0-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="e02e0-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="e02e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e02e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e02e0-103">在虛擬網路中測試私人 IP 位址的可用性。</span><span class="sxs-lookup"><span data-stu-id="e02e0-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e02e0-104">SYNTAX</span></span>

### <span data-ttu-id="e02e0-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="e02e0-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02e0-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="e02e0-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e02e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="e02e0-107">DESCRIPTION</span></span>
<span data-ttu-id="e02e0-108">**Test AzureRmPrivateIPAddressAvailability** Cmdlet 會測試指定的私人 IP 位址是否可在虛擬網路中使用。</span><span class="sxs-lookup"><span data-stu-id="e02e0-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="e02e0-109">如果採取要求的私人 IP 位址，這個 Cmdlet 會傳回可用的私人 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="e02e0-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="e02e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="e02e0-110">EXAMPLES</span></span>

### <span data-ttu-id="e02e0-111">範例1：使用管線測試 IP 位址是否可用</span><span class="sxs-lookup"><span data-stu-id="e02e0-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="e02e0-112">這個命令會取得虛擬網路，並使用管線運算子將它傳遞給 **Test AzureRmPrivateIPAddressAvailability** ，以測試指定的私人 IP 位址是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="e02e0-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="e02e0-113">參數</span><span class="sxs-lookup"><span data-stu-id="e02e0-113">PARAMETERS</span></span>

### <span data-ttu-id="e02e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02e0-114">-DefaultProfile</span></span>
<span data-ttu-id="e02e0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e02e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02e0-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e02e0-116">-IPAddress</span></span>
<span data-ttu-id="e02e0-117">指定要測試的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e02e0-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="e02e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="e02e0-119">指定虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e02e0-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="e02e0-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e02e0-120">-VirtualNetwork</span></span>
<span data-ttu-id="e02e0-121">指定 **PSVirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="e02e0-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="e02e0-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e02e0-122">-VirtualNetworkName</span></span>
<span data-ttu-id="e02e0-123">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e02e0-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="e02e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02e0-124">CommonParameters</span></span>
<span data-ttu-id="e02e0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e02e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02e0-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e02e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02e0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e02e0-127">INPUTS</span></span>

### <span data-ttu-id="e02e0-128">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e02e0-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="e02e0-129">參數： VirtualNetwork (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e02e0-129">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="e02e0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e02e0-130">OUTPUTS</span></span>

### <span data-ttu-id="e02e0-131">PSIPAddressAvailabilityResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e02e0-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="e02e0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e02e0-132">NOTES</span></span>

## <span data-ttu-id="e02e0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e02e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="e02e0-134">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e02e0-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


