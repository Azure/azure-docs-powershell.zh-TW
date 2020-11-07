---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967498"
---
# <span data-ttu-id="135f5-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="135f5-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="135f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="135f5-102">SYNOPSIS</span></span>
<span data-ttu-id="135f5-103">設定 Azure RemoteApp 虛擬網路的屬性。</span><span class="sxs-lookup"><span data-stu-id="135f5-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="135f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="135f5-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="135f5-105">說明</span><span class="sxs-lookup"><span data-stu-id="135f5-105">DESCRIPTION</span></span>
<span data-ttu-id="135f5-106">**AzureRemoteAppVNet** Cmdlet 會設定 Azure RemoteApp 虛擬網路的屬性。</span><span class="sxs-lookup"><span data-stu-id="135f5-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="135f5-107">示例</span><span class="sxs-lookup"><span data-stu-id="135f5-107">EXAMPLES</span></span>

### <span data-ttu-id="135f5-108">範例1：設定虛擬網路的屬性</span><span class="sxs-lookup"><span data-stu-id="135f5-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="135f5-109">這個命令會設定名為 ContosoVNet 的虛擬網路的屬性。</span><span class="sxs-lookup"><span data-stu-id="135f5-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="135f5-110">參數</span><span class="sxs-lookup"><span data-stu-id="135f5-110">PARAMETERS</span></span>

### <span data-ttu-id="135f5-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="135f5-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="135f5-112">指定 DNS 伺服器的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="135f5-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="135f5-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="135f5-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="135f5-114">指定本機網路位址空間，在 Inter-Domain 路由 (CIDR) 符號中的類別中。</span><span class="sxs-lookup"><span data-stu-id="135f5-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="135f5-115">這不能與虛擬網路位址空間重迭。</span><span class="sxs-lookup"><span data-stu-id="135f5-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="135f5-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="135f5-116">-Profile</span></span>
<span data-ttu-id="135f5-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="135f5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="135f5-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="135f5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="135f5-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="135f5-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="135f5-120">指定 CIDR 符號中的虛擬網路位址空間。</span><span class="sxs-lookup"><span data-stu-id="135f5-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="135f5-121">這必須位於私有 IP 位址範圍，且無法與本機網路位址空間重迭。</span><span class="sxs-lookup"><span data-stu-id="135f5-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="135f5-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="135f5-122">-VNetName</span></span>
<span data-ttu-id="135f5-123">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="135f5-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="135f5-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="135f5-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="135f5-125">指定虛擬私人網路 (VPN) 裝置的位址。</span><span class="sxs-lookup"><span data-stu-id="135f5-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="135f5-126">這必須是公開的位址。</span><span class="sxs-lookup"><span data-stu-id="135f5-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="135f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135f5-127">CommonParameters</span></span>
<span data-ttu-id="135f5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="135f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135f5-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="135f5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135f5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="135f5-130">INPUTS</span></span>

## <span data-ttu-id="135f5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="135f5-131">OUTPUTS</span></span>

## <span data-ttu-id="135f5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="135f5-132">NOTES</span></span>

## <span data-ttu-id="135f5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="135f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="135f5-134">AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="135f5-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


