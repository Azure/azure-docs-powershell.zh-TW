---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135950"
---
# <span data-ttu-id="c394e-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="c394e-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="c394e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c394e-102">SYNOPSIS</span></span>
<span data-ttu-id="c394e-103">取得可用的 Azure 防火牆 Fqdn 標記。</span><span class="sxs-lookup"><span data-stu-id="c394e-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="c394e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c394e-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c394e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c394e-105">DESCRIPTION</span></span>
<span data-ttu-id="c394e-106">**AzFirewallFqdnTag** Cmdlet 會取得可用於 Azure 防火牆應用程式規則的 FQDN 標記清單</span><span class="sxs-lookup"><span data-stu-id="c394e-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="c394e-107">示例</span><span class="sxs-lookup"><span data-stu-id="c394e-107">EXAMPLES</span></span>

### <span data-ttu-id="c394e-108">1：檢索所有可用的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="c394e-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="c394e-109">這個範例會檢索所有可用的 FQDN 標記。</span><span class="sxs-lookup"><span data-stu-id="c394e-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="c394e-110">2：在應用程式規則中使用第一個可用的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="c394e-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="c394e-111">這個範例會使用第一個可用的 FQDN 標記來建立防火牆應用程式規則</span><span class="sxs-lookup"><span data-stu-id="c394e-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="c394e-112">參數</span><span class="sxs-lookup"><span data-stu-id="c394e-112">PARAMETERS</span></span>

### <span data-ttu-id="c394e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c394e-113">-DefaultProfile</span></span>
<span data-ttu-id="c394e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c394e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c394e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c394e-115">CommonParameters</span></span>
<span data-ttu-id="c394e-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c394e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c394e-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c394e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c394e-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c394e-118">INPUTS</span></span>

### <span data-ttu-id="c394e-119">所有</span><span class="sxs-lookup"><span data-stu-id="c394e-119">None</span></span>

## <span data-ttu-id="c394e-120">輸出</span><span class="sxs-lookup"><span data-stu-id="c394e-120">OUTPUTS</span></span>

### <span data-ttu-id="c394e-121">PSAzureFirewallFqdnTag 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c394e-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="c394e-122">System.object. IEnumerable ' 1 [PSAzureFirewallFqdnTag，#..... Network，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="c394e-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c394e-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c394e-123">NOTES</span></span>

## <span data-ttu-id="c394e-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="c394e-124">RELATED LINKS</span></span>

[<span data-ttu-id="c394e-125">新-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c394e-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="c394e-126">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c394e-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
