---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281990"
---
# <span data-ttu-id="82061-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="82061-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="82061-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82061-102">SYNOPSIS</span></span>
<span data-ttu-id="82061-103">針對 Azure 防火牆原則建立新的 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="82061-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="82061-104">句法</span><span class="sxs-lookup"><span data-stu-id="82061-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82061-105">說明</span><span class="sxs-lookup"><span data-stu-id="82061-105">DESCRIPTION</span></span>
<span data-ttu-id="82061-106">**新的 AzFirewallPolicyDnsSetting** Cmdlet 會針對 Azure 防火牆原則建立 DNS 設定物件</span><span class="sxs-lookup"><span data-stu-id="82061-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="82061-107">示例</span><span class="sxs-lookup"><span data-stu-id="82061-107">EXAMPLES</span></span>

### <span data-ttu-id="82061-108">1. 建立空白原則</span><span class="sxs-lookup"><span data-stu-id="82061-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="82061-109">這個範例會建立設定啟用 dns proxy 的 dns 設定物件。</span><span class="sxs-lookup"><span data-stu-id="82061-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="82061-110">2. 使用 ThreatIntel 模式建立空原則</span><span class="sxs-lookup"><span data-stu-id="82061-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="82061-111">這個範例會建立一個 dns 設定物件，並設定啟用 dns proxy 及設定自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="82061-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="82061-112">參數</span><span class="sxs-lookup"><span data-stu-id="82061-112">PARAMETERS</span></span>

### <span data-ttu-id="82061-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82061-113">-DefaultProfile</span></span>
<span data-ttu-id="82061-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82061-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82061-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="82061-115">-EnableProxy</span></span>
<span data-ttu-id="82061-116">[啟用 DNS Proxy]。</span><span class="sxs-lookup"><span data-stu-id="82061-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="82061-117">預設為停用。</span><span class="sxs-lookup"><span data-stu-id="82061-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="82061-118">-伺服器</span><span class="sxs-lookup"><span data-stu-id="82061-118">-Server</span></span>
<span data-ttu-id="82061-119">DNS 伺服器清單</span><span class="sxs-lookup"><span data-stu-id="82061-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="82061-120">-確認</span><span class="sxs-lookup"><span data-stu-id="82061-120">-Confirm</span></span>
<span data-ttu-id="82061-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82061-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82061-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82061-122">-WhatIf</span></span>
<span data-ttu-id="82061-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82061-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82061-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82061-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82061-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82061-125">CommonParameters</span></span>
<span data-ttu-id="82061-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82061-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82061-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="82061-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82061-128">輸入</span><span class="sxs-lookup"><span data-stu-id="82061-128">INPUTS</span></span>

### <span data-ttu-id="82061-129">所有</span><span class="sxs-lookup"><span data-stu-id="82061-129">None</span></span>

## <span data-ttu-id="82061-130">輸出</span><span class="sxs-lookup"><span data-stu-id="82061-130">OUTPUTS</span></span>

### <span data-ttu-id="82061-131">PSAzureFirewallPolicyDnsSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82061-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="82061-132">筆記</span><span class="sxs-lookup"><span data-stu-id="82061-132">NOTES</span></span>

## <span data-ttu-id="82061-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="82061-133">RELATED LINKS</span></span>
