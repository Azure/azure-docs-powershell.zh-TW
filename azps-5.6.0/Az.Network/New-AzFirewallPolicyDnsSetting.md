---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 35b56e6aafe73c09343fb17d385dd7ab4c705c5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910414"
---
# <span data-ttu-id="2fb02-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="2fb02-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="2fb02-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2fb02-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb02-103">為 Azure 防火牆政策建立新的 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="2fb02-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="2fb02-104">語法</span><span class="sxs-lookup"><span data-stu-id="2fb02-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb02-105">描述</span><span class="sxs-lookup"><span data-stu-id="2fb02-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb02-106">**New-AzFirewallPolicyDnsSetting** Cmdlet 會為 Azure 防火牆策略建立 DNS 設定物件</span><span class="sxs-lookup"><span data-stu-id="2fb02-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="2fb02-107">例子</span><span class="sxs-lookup"><span data-stu-id="2fb02-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb02-108">1. 建立空白政策</span><span class="sxs-lookup"><span data-stu-id="2fb02-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="2fb02-109">此範例會建立設定啟用 dns Proxy 的 dns 設定物件。</span><span class="sxs-lookup"><span data-stu-id="2fb02-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="2fb02-110">2. 使用 ThreatIntel 模式建立空白策略</span><span class="sxs-lookup"><span data-stu-id="2fb02-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="2fb02-111">此範例會建立設定啟用 dns Proxy 和設定自訂 dns 伺服器的 dns 設定物件。</span><span class="sxs-lookup"><span data-stu-id="2fb02-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="2fb02-112">參數</span><span class="sxs-lookup"><span data-stu-id="2fb02-112">PARAMETERS</span></span>

### <span data-ttu-id="2fb02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb02-113">-DefaultProfile</span></span>
<span data-ttu-id="2fb02-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fb02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fb02-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="2fb02-115">-EnableProxy</span></span>
<span data-ttu-id="2fb02-116">啟用 DNS Proxy。</span><span class="sxs-lookup"><span data-stu-id="2fb02-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="2fb02-117">根據預設，它會停用。</span><span class="sxs-lookup"><span data-stu-id="2fb02-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="2fb02-118">-Server</span><span class="sxs-lookup"><span data-stu-id="2fb02-118">-Server</span></span>
<span data-ttu-id="2fb02-119">DNS 伺服器清單</span><span class="sxs-lookup"><span data-stu-id="2fb02-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="2fb02-120">-確認</span><span class="sxs-lookup"><span data-stu-id="2fb02-120">-Confirm</span></span>
<span data-ttu-id="2fb02-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2fb02-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb02-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb02-122">-WhatIf</span></span>
<span data-ttu-id="2fb02-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fb02-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb02-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fb02-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb02-125">CommonParameters</span></span>
<span data-ttu-id="2fb02-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2fb02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb02-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fb02-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb02-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2fb02-128">INPUTS</span></span>

### <span data-ttu-id="2fb02-129">沒有</span><span class="sxs-lookup"><span data-stu-id="2fb02-129">None</span></span>

## <span data-ttu-id="2fb02-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2fb02-130">OUTPUTS</span></span>

### <span data-ttu-id="2fb02-131">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="2fb02-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="2fb02-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2fb02-132">NOTES</span></span>

## <span data-ttu-id="2fb02-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fb02-133">RELATED LINKS</span></span>
