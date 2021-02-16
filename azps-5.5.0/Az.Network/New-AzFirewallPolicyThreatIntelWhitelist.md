---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133847"
---
# <span data-ttu-id="9f81d-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="9f81d-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="9f81d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f81d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f81d-103">針對 Azure 防火牆原則建立新的威脅智慧白名單</span><span class="sxs-lookup"><span data-stu-id="9f81d-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="9f81d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f81d-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f81d-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f81d-105">DESCRIPTION</span></span>
<span data-ttu-id="9f81d-106">**新的-AzFirewallPolicyThreatIntelWhitelist** Cmdlet 會建立一個威脅英特爾白名單物件，可在建立或設定 Azure 防火牆原則時使用。</span><span class="sxs-lookup"><span data-stu-id="9f81d-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="9f81d-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f81d-107">EXAMPLES</span></span>

### <span data-ttu-id="9f81d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9f81d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="9f81d-109">這個範例會建立一個威脅英特爾白名單，其中包含一個專案的 FQDN 白名單，以及兩個專案的 Ip 位址白名單</span><span class="sxs-lookup"><span data-stu-id="9f81d-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="9f81d-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f81d-110">PARAMETERS</span></span>

### <span data-ttu-id="9f81d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f81d-111">-DefaultProfile</span></span>
<span data-ttu-id="9f81d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f81d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f81d-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="9f81d-113">-FQDN</span></span>
<span data-ttu-id="9f81d-114">威脅英特爾白名單的 Fqdn</span><span class="sxs-lookup"><span data-stu-id="9f81d-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="9f81d-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9f81d-115">-IpAddress</span></span>
<span data-ttu-id="9f81d-116">威脅英特爾白名單的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="9f81d-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="9f81d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f81d-117">CommonParameters</span></span>
<span data-ttu-id="9f81d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f81d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f81d-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9f81d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f81d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9f81d-120">INPUTS</span></span>

### <span data-ttu-id="9f81d-121">所有</span><span class="sxs-lookup"><span data-stu-id="9f81d-121">None</span></span>

## <span data-ttu-id="9f81d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="9f81d-122">OUTPUTS</span></span>

### <span data-ttu-id="9f81d-123">PSAzureFirewallPolicyThreatIntelWhitelist 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9f81d-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="9f81d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="9f81d-124">NOTES</span></span>

## <span data-ttu-id="9f81d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f81d-125">RELATED LINKS</span></span>
