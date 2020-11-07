---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967440"
---
# <span data-ttu-id="73642-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="73642-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="73642-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73642-102">SYNOPSIS</span></span>
<span data-ttu-id="73642-103">建立 Azure RemoteApp 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="73642-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="73642-104">句法</span><span class="sxs-lookup"><span data-stu-id="73642-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73642-105">說明</span><span class="sxs-lookup"><span data-stu-id="73642-105">DESCRIPTION</span></span>
<span data-ttu-id="73642-106">**新的-AzureRemoteAppVNet** Cmdlet 會建立 Azure RemoteApp 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="73642-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="73642-107">示例</span><span class="sxs-lookup"><span data-stu-id="73642-107">EXAMPLES</span></span>

### <span data-ttu-id="73642-108">範例1：建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="73642-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="73642-109">這個命令會建立名為 ContosoVNet 的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="73642-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="73642-110">若要判斷作業的狀態，請使用 **AzureRemoteAppOperationResult** Cmdlet 以及此 Cmdlet 傳回的追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="73642-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="73642-111">參數</span><span class="sxs-lookup"><span data-stu-id="73642-111">PARAMETERS</span></span>

### <span data-ttu-id="73642-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="73642-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="73642-113">指定 DNS 伺服器的 IPv4 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="73642-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-114">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="73642-114">-GatewayType</span></span>
<span data-ttu-id="73642-115">指定要使用的閘道路由類型。</span><span class="sxs-lookup"><span data-stu-id="73642-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="73642-116">此參數可接受的值為： StaticRouting 或 DynamicRouting。</span><span class="sxs-lookup"><span data-stu-id="73642-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="73642-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="73642-118">指定指定本機網路位址空間的字串陣列，這些字串是在無類別域間路由 (CIDR) 符號。</span><span class="sxs-lookup"><span data-stu-id="73642-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="73642-119">此位址空間不得與 *VirtualNetworkAddressSpace* 參數指定的虛擬網路位址空間重迭。</span><span class="sxs-lookup"><span data-stu-id="73642-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-120">-位置</span><span class="sxs-lookup"><span data-stu-id="73642-120">-Location</span></span>
<span data-ttu-id="73642-121">指定建立虛擬網路的位置。</span><span class="sxs-lookup"><span data-stu-id="73642-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="73642-122">-Profile</span></span>
<span data-ttu-id="73642-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="73642-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73642-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="73642-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73642-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="73642-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="73642-126">指定一個字串陣列，該字串指定 CIDR 符號中的虛擬網路位址空間。</span><span class="sxs-lookup"><span data-stu-id="73642-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="73642-127">這必須位於私有 IP 位址範圍，且無法與 *LocalNetworkAddressSpace* 參數指定的本機網路位址空間重迭。</span><span class="sxs-lookup"><span data-stu-id="73642-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="73642-128">-VNetName</span></span>
<span data-ttu-id="73642-129">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="73642-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="73642-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="73642-131">指定虛擬私人網路 (VPN) 裝置的位址。</span><span class="sxs-lookup"><span data-stu-id="73642-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="73642-132">這必須是公開的位址。</span><span class="sxs-lookup"><span data-stu-id="73642-132">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73642-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73642-133">CommonParameters</span></span>
<span data-ttu-id="73642-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73642-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73642-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73642-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73642-136">輸入</span><span class="sxs-lookup"><span data-stu-id="73642-136">INPUTS</span></span>

## <span data-ttu-id="73642-137">輸出</span><span class="sxs-lookup"><span data-stu-id="73642-137">OUTPUTS</span></span>

## <span data-ttu-id="73642-138">筆記</span><span class="sxs-lookup"><span data-stu-id="73642-138">NOTES</span></span>

## <span data-ttu-id="73642-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="73642-139">RELATED LINKS</span></span>

[<span data-ttu-id="73642-140">AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="73642-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="73642-141">AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="73642-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="73642-142">移除-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="73642-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="73642-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="73642-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


