---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966936"
---
# <span data-ttu-id="a1364-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a1364-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="a1364-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1364-102">SYNOPSIS</span></span>
<span data-ttu-id="a1364-103">刪除 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="a1364-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="a1364-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1364-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1364-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1364-105">DESCRIPTION</span></span>
<span data-ttu-id="a1364-106">**AzureVNetGateway** Cmdlet 會將現有的虛擬私人網路 (VPN) 閘道的虛擬網路上刪除。</span><span class="sxs-lookup"><span data-stu-id="a1364-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="a1364-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1364-107">EXAMPLES</span></span>

### <span data-ttu-id="a1364-108">範例1：移除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a1364-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="a1364-109">這個命令會從名為 ContosoVN07 的虛擬網路中移除虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a1364-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="a1364-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1364-110">PARAMETERS</span></span>

### <span data-ttu-id="a1364-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a1364-111">-Profile</span></span>
<span data-ttu-id="a1364-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a1364-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a1364-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a1364-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1364-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a1364-114">-VNetName</span></span>
<span data-ttu-id="a1364-115">指定此 Cmdlet 刪除 VPN 閘道的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a1364-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="a1364-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1364-116">CommonParameters</span></span>
<span data-ttu-id="a1364-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1364-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1364-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1364-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1364-119">輸入</span><span class="sxs-lookup"><span data-stu-id="a1364-119">INPUTS</span></span>

## <span data-ttu-id="a1364-120">輸出</span><span class="sxs-lookup"><span data-stu-id="a1364-120">OUTPUTS</span></span>

## <span data-ttu-id="a1364-121">筆記</span><span class="sxs-lookup"><span data-stu-id="a1364-121">NOTES</span></span>

## <span data-ttu-id="a1364-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1364-122">RELATED LINKS</span></span>

[<span data-ttu-id="a1364-123">AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a1364-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="a1364-124">新-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a1364-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="a1364-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a1364-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="a1364-126">調整大小-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a1364-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="a1364-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a1364-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


