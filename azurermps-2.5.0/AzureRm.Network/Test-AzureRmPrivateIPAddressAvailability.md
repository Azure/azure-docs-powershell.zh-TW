---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
ms.openlocfilehash: 73924c1d1308a4cf457033e27e49ad7f9e19392e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800310"
---
# <span data-ttu-id="ada4f-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="ada4f-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="ada4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ada4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ada4f-103">在虛擬網路中測試私人 IP 位址的可用性。</span><span class="sxs-lookup"><span data-stu-id="ada4f-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ada4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ada4f-104">SYNTAX</span></span>

### <span data-ttu-id="ada4f-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="ada4f-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ada4f-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="ada4f-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada4f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ada4f-107">DESCRIPTION</span></span>
<span data-ttu-id="ada4f-108">**Test AzureRmPrivateIPAddressAvailability** Cmdlet 會測試指定的私人 IP 位址是否可在虛擬網路中使用。</span><span class="sxs-lookup"><span data-stu-id="ada4f-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="ada4f-109">如果採取要求的私人 IP 位址，這個 Cmdlet 會傳回可用的私人 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="ada4f-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="ada4f-110">示例</span><span class="sxs-lookup"><span data-stu-id="ada4f-110">EXAMPLES</span></span>

### <span data-ttu-id="ada4f-111">範例1：使用管線測試 IP 位址是否可用</span><span class="sxs-lookup"><span data-stu-id="ada4f-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="ada4f-112">這個命令會取得虛擬網路，並使用管線運算子將它傳遞給 **Test AzureRmPrivateIPAddressAvailability** ，以測試指定的私人 IP 位址是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="ada4f-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="ada4f-113">參數</span><span class="sxs-lookup"><span data-stu-id="ada4f-113">PARAMETERS</span></span>

### <span data-ttu-id="ada4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada4f-114">-DefaultProfile</span></span>
<span data-ttu-id="ada4f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ada4f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4f-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="ada4f-116">-IPAddress</span></span>
<span data-ttu-id="ada4f-117">指定要測試的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ada4f-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="ada4f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada4f-118">-ResourceGroupName</span></span>
<span data-ttu-id="ada4f-119">指定虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ada4f-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4f-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ada4f-120">-VirtualNetwork</span></span>
<span data-ttu-id="ada4f-121">指定 **PSVirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="ada4f-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ada4f-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ada4f-122">-VirtualNetworkName</span></span>
<span data-ttu-id="ada4f-123">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="ada4f-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada4f-124">CommonParameters</span></span>
<span data-ttu-id="ada4f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ada4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada4f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ada4f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada4f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ada4f-127">INPUTS</span></span>

### <span data-ttu-id="ada4f-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ada4f-128">PSVirtualNetwork</span></span>
<span data-ttu-id="ada4f-129">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ada4f-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ada4f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ada4f-130">OUTPUTS</span></span>

### <span data-ttu-id="ada4f-131">PSIPAddressAvailabilityResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ada4f-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="ada4f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ada4f-132">NOTES</span></span>

## <span data-ttu-id="ada4f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ada4f-133">RELATED LINKS</span></span>

[<span data-ttu-id="ada4f-134">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ada4f-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


