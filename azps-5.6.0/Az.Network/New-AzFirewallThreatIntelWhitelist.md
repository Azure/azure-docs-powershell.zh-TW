---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904961"
---
# <span data-ttu-id="fba47-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="fba47-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="fba47-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fba47-102">SYNOPSIS</span></span>
<span data-ttu-id="fba47-103">為 Azure 防火牆建立新的威脅情報白名單</span><span class="sxs-lookup"><span data-stu-id="fba47-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="fba47-104">語法</span><span class="sxs-lookup"><span data-stu-id="fba47-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba47-105">描述</span><span class="sxs-lookup"><span data-stu-id="fba47-105">DESCRIPTION</span></span>
<span data-ttu-id="fba47-106">**New-AzFirewallThreatIntelWhitelist** Cmdlet 會建立威脅 intel whitelist 物件，可用於建立或設定 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="fba47-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="fba47-107">例子</span><span class="sxs-lookup"><span data-stu-id="fba47-107">EXAMPLES</span></span>

### <span data-ttu-id="fba47-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fba47-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="fba47-109">此範例會建立一個威脅 Intel Whitelist，其中包含一個包含兩個輸入的 FQDN 白名單，以及一個包含兩個輸入的 Ip 位址白名單</span><span class="sxs-lookup"><span data-stu-id="fba47-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="fba47-110">參數</span><span class="sxs-lookup"><span data-stu-id="fba47-110">PARAMETERS</span></span>

### <span data-ttu-id="fba47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba47-111">-DefaultProfile</span></span>
<span data-ttu-id="fba47-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fba47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba47-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="fba47-113">-FQDN</span></span>
<span data-ttu-id="fba47-114">Threat Intel Whitelist 的 FQNS</span><span class="sxs-lookup"><span data-stu-id="fba47-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba47-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="fba47-115">-IpAddress</span></span>
<span data-ttu-id="fba47-116">Threat Intel Whitelist 的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="fba47-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba47-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba47-117">CommonParameters</span></span>
<span data-ttu-id="fba47-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fba47-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba47-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fba47-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba47-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fba47-120">INPUTS</span></span>

### <span data-ttu-id="fba47-121">沒有</span><span class="sxs-lookup"><span data-stu-id="fba47-121">None</span></span>

## <span data-ttu-id="fba47-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fba47-122">OUTPUTS</span></span>

### <span data-ttu-id="fba47-123">Microsoft.Azure.Commands.Network.models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="fba47-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="fba47-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fba47-124">NOTES</span></span>

## <span data-ttu-id="fba47-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fba47-125">RELATED LINKS</span></span>

[<span data-ttu-id="fba47-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fba47-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="fba47-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fba47-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="fba47-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fba47-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)