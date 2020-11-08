---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138019"
---
# <span data-ttu-id="a23ac-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a23ac-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a23ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a23ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a23ac-103">將私人連結設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a23ac-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="a23ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a23ac-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a23ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="a23ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a23ac-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會將私人連結設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a23ac-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="a23ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="a23ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a23ac-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a23ac-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="a23ac-109">第一個命令會建立 privateLinkIpConfiguration，並將它儲存在 $PrivateLinkIpConfiguration 變數中。</span><span class="sxs-lookup"><span data-stu-id="a23ac-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="a23ac-110">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，然後將其儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a23ac-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a23ac-111">第三個命令會針對 $AppGw 中的閘道，新增名為 privateLinkConfig01 的私人連結設定</span><span class="sxs-lookup"><span data-stu-id="a23ac-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="a23ac-112">參數</span><span class="sxs-lookup"><span data-stu-id="a23ac-112">PARAMETERS</span></span>

### <span data-ttu-id="a23ac-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a23ac-113">-ApplicationGateway</span></span>
<span data-ttu-id="a23ac-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a23ac-114">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a23ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23ac-115">-DefaultProfile</span></span>
<span data-ttu-id="a23ac-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a23ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23ac-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a23ac-117">-IpConfiguration</span></span>
<span data-ttu-id="a23ac-118">IpConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="a23ac-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23ac-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a23ac-119">-Name</span></span>
<span data-ttu-id="a23ac-120">PrivateLink 配置的名稱</span><span class="sxs-lookup"><span data-stu-id="a23ac-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="a23ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23ac-121">CommonParameters</span></span>
<span data-ttu-id="a23ac-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a23ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23ac-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a23ac-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23ac-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a23ac-124">INPUTS</span></span>

### <span data-ttu-id="a23ac-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a23ac-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="a23ac-126">PSApplicationGatewayPrivateLinkIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a23ac-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="a23ac-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a23ac-127">OUTPUTS</span></span>

### <span data-ttu-id="a23ac-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a23ac-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a23ac-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a23ac-129">NOTES</span></span>

## <span data-ttu-id="a23ac-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a23ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="a23ac-131">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a23ac-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a23ac-132">AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a23ac-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a23ac-133">移除-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a23ac-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a23ac-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a23ac-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)