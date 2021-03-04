---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: fc0e3ad0bcc86a0ad49450393a79c6c60540ba23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914718"
---
# <span data-ttu-id="06ba7-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="06ba7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="06ba7-103">更新私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="06ba7-103">Updates a private link service.</span></span>

## <span data-ttu-id="06ba7-104">語法</span><span class="sxs-lookup"><span data-stu-id="06ba7-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ba7-105">描述</span><span class="sxs-lookup"><span data-stu-id="06ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="06ba7-106">**Set-AzPrivateLinkService** Cmdlet 會更新私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="06ba7-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="06ba7-107">例子</span><span class="sxs-lookup"><span data-stu-id="06ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="06ba7-108">1：建立私人連結服務並更新其</span><span class="sxs-lookup"><span data-stu-id="06ba7-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="06ba7-109">此範例會建立稱為 mypls 的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="06ba7-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="06ba7-110">接著，它會從記憶體 ipConfiguratiuon 物件取代其 ipConfigurations。</span><span class="sxs-lookup"><span data-stu-id="06ba7-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="06ba7-111">接著Set-AzPrivateLinkService Cmdlet，在服務端撰寫經過修改的私人連結服務狀態。</span><span class="sxs-lookup"><span data-stu-id="06ba7-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="06ba7-112">參數</span><span class="sxs-lookup"><span data-stu-id="06ba7-112">PARAMETERS</span></span>

### <span data-ttu-id="06ba7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06ba7-113">-AsJob</span></span>
<span data-ttu-id="06ba7-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="06ba7-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ba7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ba7-115">-DefaultProfile</span></span>
<span data-ttu-id="06ba7-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06ba7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ba7-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-117">-PrivateLinkService</span></span>
<span data-ttu-id="06ba7-118">指定代表私人連結服務應設定之狀態的私人連結服務物件。</span><span class="sxs-lookup"><span data-stu-id="06ba7-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ba7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ba7-119">CommonParameters</span></span>
<span data-ttu-id="06ba7-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06ba7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ba7-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06ba7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ba7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="06ba7-122">INPUTS</span></span>

### <span data-ttu-id="06ba7-123">Microsoft.Azure.Commands.Network.models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="06ba7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="06ba7-124">OUTPUTS</span></span>

### <span data-ttu-id="06ba7-125">Microsoft.Azure.Commands.Network.models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="06ba7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="06ba7-126">NOTES</span></span>

## <span data-ttu-id="06ba7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="06ba7-127">RELATED LINKS</span></span>

[<span data-ttu-id="06ba7-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="06ba7-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="06ba7-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="06ba7-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


