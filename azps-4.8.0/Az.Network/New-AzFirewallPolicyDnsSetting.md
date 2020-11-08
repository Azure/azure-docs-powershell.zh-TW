---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 2e4179019f74a8fd85b5f0ea3471bc586864172a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136283"
---
# <span data-ttu-id="703cb-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="703cb-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="703cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="703cb-102">SYNOPSIS</span></span>
<span data-ttu-id="703cb-103">針對 Azure 防火牆原則建立新的 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="703cb-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="703cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="703cb-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-ProxyNotRequiredForNetworkRule] [-Server <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="703cb-105">說明</span><span class="sxs-lookup"><span data-stu-id="703cb-105">DESCRIPTION</span></span>
<span data-ttu-id="703cb-106">**新的 AzFirewallPolicyDnsSetting** Cmdlet 會針對 Azure 防火牆原則建立 DNS 設定物件</span><span class="sxs-lookup"><span data-stu-id="703cb-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="703cb-107">示例</span><span class="sxs-lookup"><span data-stu-id="703cb-107">EXAMPLES</span></span>

### <span data-ttu-id="703cb-108">1. 建立空白原則</span><span class="sxs-lookup"><span data-stu-id="703cb-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="703cb-109">這個範例會建立設定啟用 dns proxy 的 dns 設定物件。</span><span class="sxs-lookup"><span data-stu-id="703cb-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="703cb-110">2. 使用 ThreatIntel 模式建立空原則</span><span class="sxs-lookup"><span data-stu-id="703cb-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```
<span data-ttu-id="703cb-111">這個範例會建立一個 dns 設定物件，並設定啟用 dns proxy 及設定自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="703cb-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="703cb-112">參數</span><span class="sxs-lookup"><span data-stu-id="703cb-112">PARAMETERS</span></span>

### <span data-ttu-id="703cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703cb-113">-DefaultProfile</span></span>
<span data-ttu-id="703cb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="703cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="703cb-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="703cb-115">-EnableProxy</span></span>
<span data-ttu-id="703cb-116">[啟用 DNS Proxy]。</span><span class="sxs-lookup"><span data-stu-id="703cb-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="703cb-117">預設為停用。</span><span class="sxs-lookup"><span data-stu-id="703cb-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="703cb-118">-ProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="703cb-118">-ProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="703cb-119">在網路規則中需要 Fqdn 的 DNS Proxy 功能。</span><span class="sxs-lookup"><span data-stu-id="703cb-119">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>
<span data-ttu-id="703cb-120">預設為 true。</span><span class="sxs-lookup"><span data-stu-id="703cb-120">By default it is true.</span></span>

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

### <span data-ttu-id="703cb-121">-伺服器</span><span class="sxs-lookup"><span data-stu-id="703cb-121">-Server</span></span>
<span data-ttu-id="703cb-122">DNS 伺服器清單</span><span class="sxs-lookup"><span data-stu-id="703cb-122">The list of DNS Servers</span></span>

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

### <span data-ttu-id="703cb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="703cb-123">-Confirm</span></span>
<span data-ttu-id="703cb-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="703cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="703cb-125">-WhatIf</span></span>
<span data-ttu-id="703cb-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="703cb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="703cb-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="703cb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703cb-128">CommonParameters</span></span>
<span data-ttu-id="703cb-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="703cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703cb-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="703cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703cb-131">輸入</span><span class="sxs-lookup"><span data-stu-id="703cb-131">INPUTS</span></span>

### <span data-ttu-id="703cb-132">所有</span><span class="sxs-lookup"><span data-stu-id="703cb-132">None</span></span>

## <span data-ttu-id="703cb-133">輸出</span><span class="sxs-lookup"><span data-stu-id="703cb-133">OUTPUTS</span></span>

### <span data-ttu-id="703cb-134">PSAzureFirewallPolicyDnsSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="703cb-134">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="703cb-135">筆記</span><span class="sxs-lookup"><span data-stu-id="703cb-135">NOTES</span></span>

## <span data-ttu-id="703cb-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="703cb-136">RELATED LINKS</span></span>