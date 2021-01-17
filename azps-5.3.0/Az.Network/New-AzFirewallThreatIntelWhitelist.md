---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438863"
---
# <span data-ttu-id="a24f1-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="a24f1-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="a24f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a24f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a24f1-103">針對 Azure 防火牆建立新的威脅智慧白名單</span><span class="sxs-lookup"><span data-stu-id="a24f1-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="a24f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a24f1-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a24f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="a24f1-105">DESCRIPTION</span></span>
<span data-ttu-id="a24f1-106">**新的-AzFirewallThreatIntelWhitelist** Cmdlet 會建立一個威脅英特爾白名單物件，可在建立或設定 Azure 防火牆時使用。</span><span class="sxs-lookup"><span data-stu-id="a24f1-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="a24f1-107">示例</span><span class="sxs-lookup"><span data-stu-id="a24f1-107">EXAMPLES</span></span>

### <span data-ttu-id="a24f1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a24f1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="a24f1-109">這個範例會建立一個威脅英特爾白名單，其中包含兩個專案的 FQDN 白名單，以及兩個專案的 Ip 位址白名單</span><span class="sxs-lookup"><span data-stu-id="a24f1-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="a24f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="a24f1-110">PARAMETERS</span></span>

### <span data-ttu-id="a24f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24f1-111">-DefaultProfile</span></span>
<span data-ttu-id="a24f1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a24f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a24f1-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="a24f1-113">-FQDN</span></span>
<span data-ttu-id="a24f1-114">威脅英特爾白名單的 Fqdn</span><span class="sxs-lookup"><span data-stu-id="a24f1-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="a24f1-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a24f1-115">-IpAddress</span></span>
<span data-ttu-id="a24f1-116">威脅英特爾白名單的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="a24f1-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="a24f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24f1-117">CommonParameters</span></span>
<span data-ttu-id="a24f1-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a24f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24f1-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a24f1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24f1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a24f1-120">INPUTS</span></span>

### <span data-ttu-id="a24f1-121">所有</span><span class="sxs-lookup"><span data-stu-id="a24f1-121">None</span></span>

## <span data-ttu-id="a24f1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a24f1-122">OUTPUTS</span></span>

### <span data-ttu-id="a24f1-123">PSAzureFirewallThreatIntelWhitelist 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a24f1-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="a24f1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a24f1-124">NOTES</span></span>

## <span data-ttu-id="a24f1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a24f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="a24f1-126">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a24f1-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="a24f1-127">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a24f1-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a24f1-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a24f1-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)