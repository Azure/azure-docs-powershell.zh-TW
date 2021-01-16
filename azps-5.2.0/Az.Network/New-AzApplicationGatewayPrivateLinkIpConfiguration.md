---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276348"
---
# <span data-ttu-id="450b6-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="450b6-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="450b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="450b6-102">SYNOPSIS</span></span>
<span data-ttu-id="450b6-103">建立與 PrivateLink 設定相關聯的 Ip 配置</span><span class="sxs-lookup"><span data-stu-id="450b6-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="450b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="450b6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="450b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="450b6-105">DESCRIPTION</span></span>
<span data-ttu-id="450b6-106">**新的-AzApplicationGatewayPrivateLinkIpConfiguration** Cmdlet 會建立一個 Ip 配置，以與 Azure 應用程式閘道的 PrivateLink 設定相關聯。</span><span class="sxs-lookup"><span data-stu-id="450b6-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="450b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="450b6-107">EXAMPLES</span></span>

### <span data-ttu-id="450b6-108">範例1： PrivateLink Ip 配置</span><span class="sxs-lookup"><span data-stu-id="450b6-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="450b6-109">這個命令會建立名為 "ipConfig01" 的 PrivateLink IP 配置，將結果儲存在名為 $PrivateLinkIpConfiguration 的變數中。</span><span class="sxs-lookup"><span data-stu-id="450b6-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="450b6-110">參數</span><span class="sxs-lookup"><span data-stu-id="450b6-110">PARAMETERS</span></span>

### <span data-ttu-id="450b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450b6-111">-DefaultProfile</span></span>
<span data-ttu-id="450b6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="450b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450b6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="450b6-113">-Name</span></span>
<span data-ttu-id="450b6-114">IpConfiguration 的名稱</span><span class="sxs-lookup"><span data-stu-id="450b6-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="450b6-115">-主要</span><span class="sxs-lookup"><span data-stu-id="450b6-115">-Primary</span></span>
<span data-ttu-id="450b6-116">指出 ip 設定為主要。</span><span class="sxs-lookup"><span data-stu-id="450b6-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="450b6-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="450b6-117">-PrivateIpAddress</span></span>
<span data-ttu-id="450b6-118">如果需要靜態配置，則為 ipConfiguration 的專用 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="450b6-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="450b6-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="450b6-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="450b6-120">Ip 版本的 ip 配置</span><span class="sxs-lookup"><span data-stu-id="450b6-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="450b6-121">-子網</span><span class="sxs-lookup"><span data-stu-id="450b6-121">-Subnet</span></span>
<span data-ttu-id="450b6-122">端子</span><span class="sxs-lookup"><span data-stu-id="450b6-122">Subnet</span></span>

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

### <span data-ttu-id="450b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450b6-123">CommonParameters</span></span>
<span data-ttu-id="450b6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="450b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450b6-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="450b6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450b6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="450b6-126">INPUTS</span></span>

### <span data-ttu-id="450b6-127">所有</span><span class="sxs-lookup"><span data-stu-id="450b6-127">None</span></span>

## <span data-ttu-id="450b6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="450b6-128">OUTPUTS</span></span>

### <span data-ttu-id="450b6-129">PSApplicationGatewayPrivateLinkIpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="450b6-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="450b6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="450b6-130">NOTES</span></span>

## <span data-ttu-id="450b6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="450b6-131">RELATED LINKS</span></span>

[<span data-ttu-id="450b6-132">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="450b6-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
