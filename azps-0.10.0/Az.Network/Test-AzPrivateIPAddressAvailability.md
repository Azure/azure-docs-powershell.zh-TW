---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 6a5ee3b03a4242c3c11d5c34da4a333ee7c82843
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795355"
---
# <span data-ttu-id="23df6-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="23df6-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="23df6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23df6-102">SYNOPSIS</span></span>
<span data-ttu-id="23df6-103">在虛擬網路中測試私人 IP 位址的可用性。</span><span class="sxs-lookup"><span data-stu-id="23df6-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="23df6-104">句法</span><span class="sxs-lookup"><span data-stu-id="23df6-104">SYNTAX</span></span>

### <span data-ttu-id="23df6-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="23df6-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23df6-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="23df6-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23df6-107">說明</span><span class="sxs-lookup"><span data-stu-id="23df6-107">DESCRIPTION</span></span>
<span data-ttu-id="23df6-108">**Test AzPrivateIPAddressAvailability** Cmdlet 會測試指定的私人 IP 位址是否可在虛擬網路中使用。</span><span class="sxs-lookup"><span data-stu-id="23df6-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="23df6-109">如果採取要求的私人 IP 位址，這個 Cmdlet 會傳回可用的私人 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="23df6-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="23df6-110">示例</span><span class="sxs-lookup"><span data-stu-id="23df6-110">EXAMPLES</span></span>

### <span data-ttu-id="23df6-111">範例1：使用管線測試 IP 位址是否可用</span><span class="sxs-lookup"><span data-stu-id="23df6-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="23df6-112">這個命令會取得虛擬網路，並使用管線運算子將它傳遞給 **Test AzPrivateIPAddressAvailability** ，以測試指定的私人 IP 位址是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="23df6-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="23df6-113">參數</span><span class="sxs-lookup"><span data-stu-id="23df6-113">PARAMETERS</span></span>

### <span data-ttu-id="23df6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23df6-114">-DefaultProfile</span></span>
<span data-ttu-id="23df6-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23df6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23df6-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="23df6-116">-IPAddress</span></span>
<span data-ttu-id="23df6-117">指定要測試的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="23df6-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="23df6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23df6-118">-ResourceGroupName</span></span>
<span data-ttu-id="23df6-119">指定虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23df6-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="23df6-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23df6-120">-VirtualNetwork</span></span>
<span data-ttu-id="23df6-121">指定 **PSVirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="23df6-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="23df6-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="23df6-122">-VirtualNetworkName</span></span>
<span data-ttu-id="23df6-123">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="23df6-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="23df6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23df6-124">CommonParameters</span></span>
<span data-ttu-id="23df6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23df6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23df6-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23df6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23df6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="23df6-127">INPUTS</span></span>

### <span data-ttu-id="23df6-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23df6-128">PSVirtualNetwork</span></span>
<span data-ttu-id="23df6-129">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="23df6-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="23df6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="23df6-130">OUTPUTS</span></span>

### <span data-ttu-id="23df6-131">PSIPAddressAvailabilityResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23df6-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="23df6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="23df6-132">NOTES</span></span>

## <span data-ttu-id="23df6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="23df6-133">RELATED LINKS</span></span>

[<span data-ttu-id="23df6-134">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23df6-134">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


