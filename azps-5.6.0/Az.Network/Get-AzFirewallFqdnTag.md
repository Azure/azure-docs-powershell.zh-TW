---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903158"
---
# <span data-ttu-id="e3319-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e3319-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="e3319-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3319-102">SYNOPSIS</span></span>
<span data-ttu-id="e3319-103">獲得可用的 Azure 防火牆 Fqdn 標記。</span><span class="sxs-lookup"><span data-stu-id="e3319-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="e3319-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3319-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3319-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3319-105">DESCRIPTION</span></span>
<span data-ttu-id="e3319-106">**Get-AzFirewallFqdnTag** Cmdlet 會取得 FQDN 標籤清單，可用於 Azure 防火牆應用程式規則</span><span class="sxs-lookup"><span data-stu-id="e3319-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="e3319-107">例子</span><span class="sxs-lookup"><span data-stu-id="e3319-107">EXAMPLES</span></span>

### <span data-ttu-id="e3319-108">1：取回所有可用的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="e3319-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="e3319-109">此範例會取回所有可用的 FQDN 標記。</span><span class="sxs-lookup"><span data-stu-id="e3319-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="e3319-110">2：在應用程式規則中使用第一個可用的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="e3319-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="e3319-111">此範例使用第一個可用的 FQDN 標記建立防火牆應用程式規則</span><span class="sxs-lookup"><span data-stu-id="e3319-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="e3319-112">參數</span><span class="sxs-lookup"><span data-stu-id="e3319-112">PARAMETERS</span></span>

### <span data-ttu-id="e3319-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3319-113">-DefaultProfile</span></span>
<span data-ttu-id="e3319-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3319-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3319-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3319-115">CommonParameters</span></span>
<span data-ttu-id="e3319-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3319-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3319-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3319-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3319-118">輸入</span><span class="sxs-lookup"><span data-stu-id="e3319-118">INPUTS</span></span>

### <span data-ttu-id="e3319-119">沒有</span><span class="sxs-lookup"><span data-stu-id="e3319-119">None</span></span>

## <span data-ttu-id="e3319-120">輸出</span><span class="sxs-lookup"><span data-stu-id="e3319-120">OUTPUTS</span></span>

### <span data-ttu-id="e3319-121">Microsoft.Azure.Commands.Network.models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e3319-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="e3319-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.models.PSAzureFirewallFqdnTag，Microsoft.Azure.PowerShell.Cmdlets.Network，Version=1.0.0.0，Culture=neutral，PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e3319-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3319-123">筆記</span><span class="sxs-lookup"><span data-stu-id="e3319-123">NOTES</span></span>

## <span data-ttu-id="e3319-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3319-124">RELATED LINKS</span></span>

[<span data-ttu-id="e3319-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e3319-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="e3319-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e3319-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
