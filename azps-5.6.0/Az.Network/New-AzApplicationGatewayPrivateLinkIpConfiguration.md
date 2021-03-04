---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 4a34899a4e6c37ad3d4c84c173d07012110dcad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910693"
---
# <span data-ttu-id="455c4-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="455c4-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="455c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="455c4-102">SYNOPSIS</span></span>
<span data-ttu-id="455c4-103">建立要與 PrivateLink 組組關聯的 Ip 組配置</span><span class="sxs-lookup"><span data-stu-id="455c4-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="455c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="455c4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="455c4-105">描述</span><span class="sxs-lookup"><span data-stu-id="455c4-105">DESCRIPTION</span></span>
<span data-ttu-id="455c4-106">**New-AzApplicationGatewayPrivateLinkIpConfiguration** Cmdlet 會建立與 Azure 應用程式閘道之 PrivateLink Configuration 相關聯的 Ip 組式。</span><span class="sxs-lookup"><span data-stu-id="455c4-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="455c4-107">例子</span><span class="sxs-lookup"><span data-stu-id="455c4-107">EXAMPLES</span></span>

### <span data-ttu-id="455c4-108">範例 1：PrivateLink Ip Configuration</span><span class="sxs-lookup"><span data-stu-id="455c4-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="455c4-109">此命令會建立名為 'ipConfig01' 的 PrivateLink IP 組$PrivateLinkIpConfiguration。</span><span class="sxs-lookup"><span data-stu-id="455c4-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="455c4-110">參數</span><span class="sxs-lookup"><span data-stu-id="455c4-110">PARAMETERS</span></span>

### <span data-ttu-id="455c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455c4-111">-DefaultProfile</span></span>
<span data-ttu-id="455c4-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="455c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="455c4-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="455c4-113">-Name</span></span>
<span data-ttu-id="455c4-114">IpConfiguration 的名稱</span><span class="sxs-lookup"><span data-stu-id="455c4-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="455c4-115">-主要</span><span class="sxs-lookup"><span data-stu-id="455c4-115">-Primary</span></span>
<span data-ttu-id="455c4-116">表示 ip 組是主要。</span><span class="sxs-lookup"><span data-stu-id="455c4-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="455c4-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="455c4-117">-PrivateIpAddress</span></span>
<span data-ttu-id="455c4-118">這是 ipConfiguration 的專用 ip 位址 ，如果需要靜態配置。</span><span class="sxs-lookup"><span data-stu-id="455c4-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="455c4-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="455c4-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="455c4-120">ip 配置的 ip 版本</span><span class="sxs-lookup"><span data-stu-id="455c4-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455c4-121">-子網</span><span class="sxs-lookup"><span data-stu-id="455c4-121">-Subnet</span></span>
<span data-ttu-id="455c4-122">子</span><span class="sxs-lookup"><span data-stu-id="455c4-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455c4-123">CommonParameters</span></span>
<span data-ttu-id="455c4-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="455c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455c4-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="455c4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455c4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="455c4-126">INPUTS</span></span>

### <span data-ttu-id="455c4-127">沒有</span><span class="sxs-lookup"><span data-stu-id="455c4-127">None</span></span>

## <span data-ttu-id="455c4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="455c4-128">OUTPUTS</span></span>

### <span data-ttu-id="455c4-129">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="455c4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="455c4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="455c4-130">NOTES</span></span>

## <span data-ttu-id="455c4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="455c4-131">RELATED LINKS</span></span>

[<span data-ttu-id="455c4-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="455c4-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
