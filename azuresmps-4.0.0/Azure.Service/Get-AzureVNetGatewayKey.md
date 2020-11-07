---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967721"
---
# <span data-ttu-id="c8e04-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c8e04-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="c8e04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8e04-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e04-103">取得虛擬網路閘道與本機網路網站之間連線的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8e04-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="c8e04-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8e04-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8e04-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8e04-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e04-106">**AzureVNetGatewayKey** Cmdlet 會針對虛擬網路閘道與本機網路網站之間的連線取得預共用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8e04-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="c8e04-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8e04-107">EXAMPLES</span></span>

## <span data-ttu-id="c8e04-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8e04-108">PARAMETERS</span></span>

### <span data-ttu-id="c8e04-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="c8e04-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="c8e04-110">指定連線至虛擬網路閘道的本機網路網站名稱。</span><span class="sxs-lookup"><span data-stu-id="c8e04-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="c8e04-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c8e04-111">-Profile</span></span>
<span data-ttu-id="c8e04-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c8e04-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c8e04-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c8e04-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8e04-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c8e04-114">-VNetName</span></span>
<span data-ttu-id="c8e04-115">指定此 Cmdlet 取得連接之共用金鑰的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c8e04-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="c8e04-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e04-116">CommonParameters</span></span>
<span data-ttu-id="c8e04-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8e04-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e04-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8e04-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e04-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c8e04-119">INPUTS</span></span>

## <span data-ttu-id="c8e04-120">輸出</span><span class="sxs-lookup"><span data-stu-id="c8e04-120">OUTPUTS</span></span>

## <span data-ttu-id="c8e04-121">筆記</span><span class="sxs-lookup"><span data-stu-id="c8e04-121">NOTES</span></span>

## <span data-ttu-id="c8e04-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8e04-122">RELATED LINKS</span></span>

[<span data-ttu-id="c8e04-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c8e04-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


