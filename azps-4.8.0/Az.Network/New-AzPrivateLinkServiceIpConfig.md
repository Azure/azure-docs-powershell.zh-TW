---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: 94375ba7d54095af131d7a61c7b06d50e2ba9521
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970344"
---
# <span data-ttu-id="5b400-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b400-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="5b400-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b400-102">SYNOPSIS</span></span>
<span data-ttu-id="5b400-103">建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="5b400-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="5b400-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b400-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b400-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b400-105">DESCRIPTION</span></span>
<span data-ttu-id="5b400-106">**新的-AzPrivateLinkServiceIpConfig** Cmdlet 會建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="5b400-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="5b400-107">此設定是用於來源 NAT 對來自專用端點的入站流量進行運算。</span><span class="sxs-lookup"><span data-stu-id="5b400-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="5b400-108">示例</span><span class="sxs-lookup"><span data-stu-id="5b400-108">EXAMPLES</span></span>

### <span data-ttu-id="5b400-109">範例1</span><span class="sxs-lookup"><span data-stu-id="5b400-109">Example 1</span></span>
```powershell
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="5b400-110">這個範例會在記憶體中建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="5b400-110">This example create a private link service ip configuration in memory.</span></span>

### <span data-ttu-id="5b400-111">範例2</span><span class="sxs-lookup"><span data-stu-id="5b400-111">Example 2</span></span>

<span data-ttu-id="5b400-112">建立私人連結服務 ip 設定。</span><span class="sxs-lookup"><span data-stu-id="5b400-112">Create a private link service ip configuration.</span></span> <span data-ttu-id="5b400-113"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="5b400-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -PrivateIpAddress '10.0.0.5' -Subnet <PSSubnet>
```

## <span data-ttu-id="5b400-114">參數</span><span class="sxs-lookup"><span data-stu-id="5b400-114">PARAMETERS</span></span>

### <span data-ttu-id="5b400-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b400-115">-DefaultProfile</span></span>
<span data-ttu-id="5b400-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b400-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b400-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b400-117">-Name</span></span>
<span data-ttu-id="5b400-118">IpConfiguration 的名稱</span><span class="sxs-lookup"><span data-stu-id="5b400-118">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="5b400-119">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b400-119">-PrivateIpAddress</span></span>
<span data-ttu-id="5b400-120">如果指定靜態配置，則為 ipConfiguration 的專用 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="5b400-120">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

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

### <span data-ttu-id="5b400-121">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5b400-121">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="5b400-122">Ip 版本的 ip 配置</span><span class="sxs-lookup"><span data-stu-id="5b400-122">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="5b400-123">-主要</span><span class="sxs-lookup"><span data-stu-id="5b400-123">-Primary</span></span>
<span data-ttu-id="5b400-124">指出目前的 ip 設定是主要的。</span><span class="sxs-lookup"><span data-stu-id="5b400-124">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="5b400-125">-子網</span><span class="sxs-lookup"><span data-stu-id="5b400-125">-Subnet</span></span>
<span data-ttu-id="5b400-126">端子</span><span class="sxs-lookup"><span data-stu-id="5b400-126">Subnet</span></span>

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

### <span data-ttu-id="5b400-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b400-127">CommonParameters</span></span>
<span data-ttu-id="5b400-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b400-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b400-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b400-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b400-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5b400-130">INPUTS</span></span>

### <span data-ttu-id="5b400-131">所有</span><span class="sxs-lookup"><span data-stu-id="5b400-131">None</span></span>

## <span data-ttu-id="5b400-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5b400-132">OUTPUTS</span></span>

### <span data-ttu-id="5b400-133">PSPrivateLinkServiceIpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5b400-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="5b400-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5b400-134">NOTES</span></span>

## <span data-ttu-id="5b400-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b400-135">RELATED LINKS</span></span>

[<span data-ttu-id="5b400-136">新-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5b400-136">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)