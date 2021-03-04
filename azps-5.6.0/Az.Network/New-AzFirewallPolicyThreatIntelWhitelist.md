---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904021"
---
# <span data-ttu-id="c5ba2-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c5ba2-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="c5ba2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ba2-103">為 Azure 防火牆政策建立新的威脅情報白名單</span><span class="sxs-lookup"><span data-stu-id="c5ba2-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="c5ba2-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5ba2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5ba2-105">描述</span><span class="sxs-lookup"><span data-stu-id="c5ba2-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ba2-106">**New-AzFirewallPolicyThreatIntelWhitelist** Cmdlet 會建立威脅 intel whitelist 物件，可用於建立或設定 Azure 防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="c5ba2-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="c5ba2-107">例子</span><span class="sxs-lookup"><span data-stu-id="c5ba2-107">EXAMPLES</span></span>

### <span data-ttu-id="c5ba2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c5ba2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="c5ba2-109">此範例會建立威脅 Intel Whitelist，其中包含一個輸入的 FQDN 白名單和兩個輸入的 Ip 位址白名單</span><span class="sxs-lookup"><span data-stu-id="c5ba2-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="c5ba2-110">參數</span><span class="sxs-lookup"><span data-stu-id="c5ba2-110">PARAMETERS</span></span>

### <span data-ttu-id="c5ba2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ba2-111">-DefaultProfile</span></span>
<span data-ttu-id="c5ba2-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5ba2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5ba2-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="c5ba2-113">-FQDN</span></span>
<span data-ttu-id="c5ba2-114">Threat Intel Whitelist 的 FQNS</span><span class="sxs-lookup"><span data-stu-id="c5ba2-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba2-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c5ba2-115">-IpAddress</span></span>
<span data-ttu-id="c5ba2-116">Threat Intel Whitelist 的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="c5ba2-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ba2-117">CommonParameters</span></span>
<span data-ttu-id="c5ba2-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5ba2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ba2-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5ba2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ba2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c5ba2-120">INPUTS</span></span>

### <span data-ttu-id="c5ba2-121">沒有</span><span class="sxs-lookup"><span data-stu-id="c5ba2-121">None</span></span>

## <span data-ttu-id="c5ba2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c5ba2-122">OUTPUTS</span></span>

### <span data-ttu-id="c5ba2-123">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c5ba2-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="c5ba2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c5ba2-124">NOTES</span></span>

## <span data-ttu-id="c5ba2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5ba2-125">RELATED LINKS</span></span>
