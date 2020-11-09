---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288216"
---
# <span data-ttu-id="9498e-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9498e-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="9498e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9498e-102">SYNOPSIS</span></span>
<span data-ttu-id="9498e-103">更新私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="9498e-103">Updates a private link service.</span></span>

## <span data-ttu-id="9498e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9498e-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9498e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9498e-105">DESCRIPTION</span></span>
<span data-ttu-id="9498e-106">**AzPrivateLinkService** Cmdlet 會更新私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="9498e-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="9498e-107">示例</span><span class="sxs-lookup"><span data-stu-id="9498e-107">EXAMPLES</span></span>

### <span data-ttu-id="9498e-108">1：建立私人連結服務並更新其</span><span class="sxs-lookup"><span data-stu-id="9498e-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="9498e-109">這個範例會建立名為 mypls 的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="9498e-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="9498e-110">接著，它會從記憶體內部 ipConfiguratiuon 物件取代其 Ipconfiguration。</span><span class="sxs-lookup"><span data-stu-id="9498e-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="9498e-111">然後使用 Set-AzPrivateLinkService Cmdlet，在服務端寫入已修改的私人連結服務狀態。</span><span class="sxs-lookup"><span data-stu-id="9498e-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="9498e-112">參數</span><span class="sxs-lookup"><span data-stu-id="9498e-112">PARAMETERS</span></span>

### <span data-ttu-id="9498e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9498e-113">-AsJob</span></span>
<span data-ttu-id="9498e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9498e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9498e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9498e-115">-DefaultProfile</span></span>
<span data-ttu-id="9498e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9498e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9498e-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9498e-117">-PrivateLinkService</span></span>
<span data-ttu-id="9498e-118">指定私人連結服務物件，該物件代表應該設定專用連結服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="9498e-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="9498e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9498e-119">CommonParameters</span></span>
<span data-ttu-id="9498e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9498e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9498e-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9498e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9498e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9498e-122">INPUTS</span></span>

### <span data-ttu-id="9498e-123">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9498e-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="9498e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9498e-124">OUTPUTS</span></span>

### <span data-ttu-id="9498e-125">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9498e-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="9498e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9498e-126">NOTES</span></span>

## <span data-ttu-id="9498e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9498e-127">RELATED LINKS</span></span>

[<span data-ttu-id="9498e-128">AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9498e-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="9498e-129">新-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9498e-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="9498e-130">移除-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9498e-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


