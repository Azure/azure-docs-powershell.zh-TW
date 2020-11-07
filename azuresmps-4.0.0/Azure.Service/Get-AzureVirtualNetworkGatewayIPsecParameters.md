---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967961"
---
# <span data-ttu-id="5e5f9-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="5e5f9-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="5e5f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e5f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5f9-103">取得 Azure 虛擬網路閘道的 IPsec 參數。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="5e5f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e5f9-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e5f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e5f9-105">DESCRIPTION</span></span>
<span data-ttu-id="5e5f9-106">**AzureVirtualNetworkGatewayIPsecParameters** Cmdlet 會取得 Azure 虛擬閘道的 IPsec 參數。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="5e5f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e5f9-107">EXAMPLES</span></span>

## <span data-ttu-id="5e5f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="5e5f9-108">PARAMETERS</span></span>

### <span data-ttu-id="5e5f9-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="5e5f9-109">-ConnectedEntityId</span></span>
<span data-ttu-id="5e5f9-110">指定已連接的 entitiy 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="5e5f9-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5e5f9-111">-GatewayId</span></span>
<span data-ttu-id="5e5f9-112">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="5e5f9-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5e5f9-113">-Profile</span></span>
<span data-ttu-id="5e5f9-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5e5f9-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e5f9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5f9-116">CommonParameters</span></span>
<span data-ttu-id="5e5f9-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5f9-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e5f9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5f9-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5e5f9-119">INPUTS</span></span>

## <span data-ttu-id="5e5f9-120">輸出</span><span class="sxs-lookup"><span data-stu-id="5e5f9-120">OUTPUTS</span></span>

## <span data-ttu-id="5e5f9-121">筆記</span><span class="sxs-lookup"><span data-stu-id="5e5f9-121">NOTES</span></span>

## <span data-ttu-id="5e5f9-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e5f9-122">RELATED LINKS</span></span>

[<span data-ttu-id="5e5f9-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="5e5f9-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


