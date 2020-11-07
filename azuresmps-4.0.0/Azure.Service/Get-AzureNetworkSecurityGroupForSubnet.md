---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967084"
---
# <span data-ttu-id="54a16-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="54a16-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="54a16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54a16-102">SYNOPSIS</span></span>
<span data-ttu-id="54a16-103">取得子網上的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="54a16-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="54a16-104">句法</span><span class="sxs-lookup"><span data-stu-id="54a16-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54a16-105">說明</span><span class="sxs-lookup"><span data-stu-id="54a16-105">DESCRIPTION</span></span>
<span data-ttu-id="54a16-106">**AzureNetworkSecurityGroupForSubnet** Cmdlet 會取得與子網相關聯的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="54a16-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="54a16-107">示例</span><span class="sxs-lookup"><span data-stu-id="54a16-107">EXAMPLES</span></span>

## <span data-ttu-id="54a16-108">參數</span><span class="sxs-lookup"><span data-stu-id="54a16-108">PARAMETERS</span></span>

### <span data-ttu-id="54a16-109">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="54a16-109">-Detailed</span></span>
<span data-ttu-id="54a16-110">表示此 Cmdlet 會顯示網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="54a16-110">Indicates that this cmdlet displays the network security rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a16-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="54a16-111">-Profile</span></span>
<span data-ttu-id="54a16-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="54a16-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54a16-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="54a16-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54a16-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="54a16-114">-SubnetName</span></span>
<span data-ttu-id="54a16-115">指定此 Cmdlet 取得網路安全性群組之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a16-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="54a16-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="54a16-116">-VirtualNetworkName</span></span>
<span data-ttu-id="54a16-117">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a16-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="54a16-118">這個 Cmdlet 會針對此參數指定的虛擬網路中的子網取得網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="54a16-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="54a16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a16-119">CommonParameters</span></span>
<span data-ttu-id="54a16-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54a16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a16-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54a16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a16-122">輸入</span><span class="sxs-lookup"><span data-stu-id="54a16-122">INPUTS</span></span>

## <span data-ttu-id="54a16-123">輸出</span><span class="sxs-lookup"><span data-stu-id="54a16-123">OUTPUTS</span></span>

## <span data-ttu-id="54a16-124">筆記</span><span class="sxs-lookup"><span data-stu-id="54a16-124">NOTES</span></span>

## <span data-ttu-id="54a16-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="54a16-125">RELATED LINKS</span></span>

[<span data-ttu-id="54a16-126">移除-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="54a16-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="54a16-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="54a16-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
