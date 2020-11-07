---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966911"
---
# <span data-ttu-id="9786f-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9786f-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="9786f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9786f-102">SYNOPSIS</span></span>
<span data-ttu-id="9786f-103">重設虛擬網路 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="9786f-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="9786f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9786f-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9786f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9786f-105">DESCRIPTION</span></span>
<span data-ttu-id="9786f-106">**Reset AzureVNetGateway** Cmdlet 會重定並重新啟動虛擬私人網路 (VPN) 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9786f-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="9786f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9786f-107">EXAMPLES</span></span>

### <span data-ttu-id="9786f-108">範例1：重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="9786f-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="9786f-109">這個命令會將虛擬網路閘道從名為 ContosoVN07 的虛擬網路重設。</span><span class="sxs-lookup"><span data-stu-id="9786f-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="9786f-110">參數</span><span class="sxs-lookup"><span data-stu-id="9786f-110">PARAMETERS</span></span>

### <span data-ttu-id="9786f-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9786f-111">-Profile</span></span>
<span data-ttu-id="9786f-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9786f-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9786f-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9786f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9786f-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9786f-114">-VNetName</span></span>
<span data-ttu-id="9786f-115">指定包含此 Cmdlet 重設之虛擬網路閘道的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="9786f-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="9786f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9786f-116">CommonParameters</span></span>
<span data-ttu-id="9786f-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9786f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9786f-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9786f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9786f-119">輸入</span><span class="sxs-lookup"><span data-stu-id="9786f-119">INPUTS</span></span>

## <span data-ttu-id="9786f-120">輸出</span><span class="sxs-lookup"><span data-stu-id="9786f-120">OUTPUTS</span></span>

## <span data-ttu-id="9786f-121">筆記</span><span class="sxs-lookup"><span data-stu-id="9786f-121">NOTES</span></span>

## <span data-ttu-id="9786f-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="9786f-122">RELATED LINKS</span></span>

[<span data-ttu-id="9786f-123">AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9786f-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="9786f-124">新-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9786f-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="9786f-125">移除-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9786f-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="9786f-126">調整大小-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9786f-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="9786f-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9786f-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


