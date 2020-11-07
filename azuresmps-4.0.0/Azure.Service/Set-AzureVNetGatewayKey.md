---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967256"
---
# <span data-ttu-id="26efc-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="26efc-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="26efc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26efc-102">SYNOPSIS</span></span>
<span data-ttu-id="26efc-103">針對 Azure VPN 閘道與本機網路網站之間的連線設定預共用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="26efc-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="26efc-104">句法</span><span class="sxs-lookup"><span data-stu-id="26efc-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26efc-105">說明</span><span class="sxs-lookup"><span data-stu-id="26efc-105">DESCRIPTION</span></span>
<span data-ttu-id="26efc-106">**AzureVNetGatewayKey** Cmdlet 會針對 Azure 虛擬私人網路 (VPN) 閘道與內部部署本機網路網站之間的連線設定預先共用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="26efc-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="26efc-107">此金鑰必須等於本機網路網站閘道所設定的金鑰。</span><span class="sxs-lookup"><span data-stu-id="26efc-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="26efc-108">如果金鑰不相符，就無法建立連線。</span><span class="sxs-lookup"><span data-stu-id="26efc-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="26efc-109">示例</span><span class="sxs-lookup"><span data-stu-id="26efc-109">EXAMPLES</span></span>

## <span data-ttu-id="26efc-110">參數</span><span class="sxs-lookup"><span data-stu-id="26efc-110">PARAMETERS</span></span>

### <span data-ttu-id="26efc-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="26efc-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="26efc-112">指定連線至虛擬網路閘道的本機網路網站名稱。</span><span class="sxs-lookup"><span data-stu-id="26efc-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="26efc-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="26efc-113">-Profile</span></span>
<span data-ttu-id="26efc-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="26efc-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="26efc-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="26efc-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26efc-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="26efc-116">-SharedKey</span></span>
<span data-ttu-id="26efc-117">指定要指派給 VPN 閘道的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="26efc-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="26efc-118">此值必須是一個長度不超過128個字元的字母數位字串。</span><span class="sxs-lookup"><span data-stu-id="26efc-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="26efc-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="26efc-119">-VNetName</span></span>
<span data-ttu-id="26efc-120">指定此 Cmdlet 為連接設定共用金鑰的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="26efc-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="26efc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26efc-121">CommonParameters</span></span>
<span data-ttu-id="26efc-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26efc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26efc-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26efc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26efc-124">輸入</span><span class="sxs-lookup"><span data-stu-id="26efc-124">INPUTS</span></span>

## <span data-ttu-id="26efc-125">輸出</span><span class="sxs-lookup"><span data-stu-id="26efc-125">OUTPUTS</span></span>

## <span data-ttu-id="26efc-126">筆記</span><span class="sxs-lookup"><span data-stu-id="26efc-126">NOTES</span></span>

## <span data-ttu-id="26efc-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="26efc-127">RELATED LINKS</span></span>

[<span data-ttu-id="26efc-128">AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="26efc-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


