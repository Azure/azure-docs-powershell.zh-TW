---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967722"
---
# <span data-ttu-id="39981-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="39981-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="39981-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39981-102">SYNOPSIS</span></span>
<span data-ttu-id="39981-103">取得虛擬網路閘道與本機網路網站之間連線的 IPsec 參數。</span><span class="sxs-lookup"><span data-stu-id="39981-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="39981-104">句法</span><span class="sxs-lookup"><span data-stu-id="39981-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39981-105">說明</span><span class="sxs-lookup"><span data-stu-id="39981-105">DESCRIPTION</span></span>
<span data-ttu-id="39981-106">**AzureVNetGatewayIPsecParameters** Cmdlet 會取得目前的網際網路通訊協定安全性 (IPsec) 和網際網路金鑰交換 (IKE) 連線網路閘道與本機網路網站之間連線的參數。</span><span class="sxs-lookup"><span data-stu-id="39981-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="39981-107">示例</span><span class="sxs-lookup"><span data-stu-id="39981-107">EXAMPLES</span></span>

## <span data-ttu-id="39981-108">參數</span><span class="sxs-lookup"><span data-stu-id="39981-108">PARAMETERS</span></span>

### <span data-ttu-id="39981-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="39981-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="39981-110">指定連線至虛擬網路閘道的本機網路網站名稱。</span><span class="sxs-lookup"><span data-stu-id="39981-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="39981-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="39981-111">-Profile</span></span>
<span data-ttu-id="39981-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="39981-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="39981-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="39981-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39981-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="39981-114">-VNetName</span></span>
<span data-ttu-id="39981-115">指定此 Cmdlet 取得連接之 IPsec 參數的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="39981-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="39981-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39981-116">CommonParameters</span></span>
<span data-ttu-id="39981-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39981-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39981-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39981-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39981-119">輸入</span><span class="sxs-lookup"><span data-stu-id="39981-119">INPUTS</span></span>

## <span data-ttu-id="39981-120">輸出</span><span class="sxs-lookup"><span data-stu-id="39981-120">OUTPUTS</span></span>

## <span data-ttu-id="39981-121">筆記</span><span class="sxs-lookup"><span data-stu-id="39981-121">NOTES</span></span>

## <span data-ttu-id="39981-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="39981-122">RELATED LINKS</span></span>

[<span data-ttu-id="39981-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="39981-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


