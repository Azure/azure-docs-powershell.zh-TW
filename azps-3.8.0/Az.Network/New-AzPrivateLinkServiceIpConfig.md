---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959199"
---
# <span data-ttu-id="ca66b-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca66b-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="ca66b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca66b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca66b-103">建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="ca66b-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="ca66b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca66b-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca66b-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca66b-105">DESCRIPTION</span></span>
<span data-ttu-id="ca66b-106">**新的-AzPrivateLinkServiceIpConfig** Cmdlet 會建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="ca66b-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="ca66b-107">此設定是用於來源 NAT 對來自專用端點的入站流量進行運算。</span><span class="sxs-lookup"><span data-stu-id="ca66b-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="ca66b-108">示例</span><span class="sxs-lookup"><span data-stu-id="ca66b-108">EXAMPLES</span></span>

### <span data-ttu-id="ca66b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ca66b-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="ca66b-110">這個範例會在記憶體中建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="ca66b-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="ca66b-111">參數</span><span class="sxs-lookup"><span data-stu-id="ca66b-111">PARAMETERS</span></span>

### <span data-ttu-id="ca66b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca66b-112">-DefaultProfile</span></span>
<span data-ttu-id="ca66b-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca66b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca66b-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca66b-114">-Name</span></span>
<span data-ttu-id="ca66b-115">IpConfiguration 的名稱</span><span class="sxs-lookup"><span data-stu-id="ca66b-115">The name of the IpConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66b-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca66b-116">-PrivateIpAddress</span></span>
<span data-ttu-id="ca66b-117">如果指定靜態配置，則為 ipConfiguration 的專用 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="ca66b-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66b-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ca66b-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="ca66b-119">Ip 版本的 ip 配置</span><span class="sxs-lookup"><span data-stu-id="ca66b-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66b-120">-主要</span><span class="sxs-lookup"><span data-stu-id="ca66b-120">-Primary</span></span>
<span data-ttu-id="ca66b-121">指出目前的 ip 設定是主要的。</span><span class="sxs-lookup"><span data-stu-id="ca66b-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="ca66b-122">-子網</span><span class="sxs-lookup"><span data-stu-id="ca66b-122">-Subnet</span></span>
<span data-ttu-id="ca66b-123">端子</span><span class="sxs-lookup"><span data-stu-id="ca66b-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca66b-124">CommonParameters</span></span>
<span data-ttu-id="ca66b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca66b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca66b-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca66b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca66b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ca66b-127">INPUTS</span></span>

### <span data-ttu-id="ca66b-128">所有</span><span class="sxs-lookup"><span data-stu-id="ca66b-128">None</span></span>

## <span data-ttu-id="ca66b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ca66b-129">OUTPUTS</span></span>

### <span data-ttu-id="ca66b-130">PSPrivateLinkServiceIpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca66b-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="ca66b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ca66b-131">NOTES</span></span>

## <span data-ttu-id="ca66b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca66b-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca66b-133">新-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca66b-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)