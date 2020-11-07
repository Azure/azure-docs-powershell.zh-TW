---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967969"
---
# <span data-ttu-id="e99a4-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e99a4-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e99a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e99a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e99a4-103">取得虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="e99a4-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="e99a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e99a4-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e99a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="e99a4-105">DESCRIPTION</span></span>
<span data-ttu-id="e99a4-106">**AzureVirtualNetworkGatewayConnection** Cmdlet 會取得 Azure 虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="e99a4-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="e99a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="e99a4-107">EXAMPLES</span></span>

## <span data-ttu-id="e99a4-108">參數</span><span class="sxs-lookup"><span data-stu-id="e99a4-108">PARAMETERS</span></span>

### <span data-ttu-id="e99a4-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="e99a4-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e99a4-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e99a4-110">Specifies the ID of a connected entity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99a4-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e99a4-111">-GatewayId</span></span>
<span data-ttu-id="e99a4-112">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="e99a4-112">Specifies the ID of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99a4-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e99a4-113">-Profile</span></span>
<span data-ttu-id="e99a4-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e99a4-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e99a4-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e99a4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e99a4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99a4-116">CommonParameters</span></span>
<span data-ttu-id="e99a4-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e99a4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99a4-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e99a4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99a4-119">輸入</span><span class="sxs-lookup"><span data-stu-id="e99a4-119">INPUTS</span></span>

## <span data-ttu-id="e99a4-120">輸出</span><span class="sxs-lookup"><span data-stu-id="e99a4-120">OUTPUTS</span></span>

## <span data-ttu-id="e99a4-121">筆記</span><span class="sxs-lookup"><span data-stu-id="e99a4-121">NOTES</span></span>

## <span data-ttu-id="e99a4-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="e99a4-122">RELATED LINKS</span></span>

[<span data-ttu-id="e99a4-123">新-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e99a4-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e99a4-124">移除-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e99a4-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e99a4-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e99a4-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
