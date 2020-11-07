---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626064"
---
# <span data-ttu-id="f063b-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="f063b-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="f063b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f063b-102">SYNOPSIS</span></span>
<span data-ttu-id="f063b-103">取得可用的 Azure 防火牆 Fqdn 標記。</span><span class="sxs-lookup"><span data-stu-id="f063b-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f063b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f063b-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f063b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f063b-105">DESCRIPTION</span></span>
<span data-ttu-id="f063b-106">**AzureRmFirewallFqdnTag** Cmdlet 會取得可用於 Azure 防火牆應用程式規則的 FQDN 標記清單</span><span class="sxs-lookup"><span data-stu-id="f063b-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="f063b-107">示例</span><span class="sxs-lookup"><span data-stu-id="f063b-107">EXAMPLES</span></span>

### <span data-ttu-id="f063b-108">1：檢索所有可用的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="f063b-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="f063b-109">這個範例會檢索所有可用的 FQDN 標記。</span><span class="sxs-lookup"><span data-stu-id="f063b-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="f063b-110">2：在應用程式規則中使用第一個可用的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="f063b-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="f063b-111">這個範例會使用第一個可用的 FQDN 標記來建立防火牆應用程式規則</span><span class="sxs-lookup"><span data-stu-id="f063b-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="f063b-112">參數</span><span class="sxs-lookup"><span data-stu-id="f063b-112">PARAMETERS</span></span>

### <span data-ttu-id="f063b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f063b-113">-DefaultProfile</span></span>
<span data-ttu-id="f063b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f063b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f063b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f063b-115">CommonParameters</span></span>
<span data-ttu-id="f063b-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f063b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f063b-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f063b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f063b-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f063b-118">INPUTS</span></span>

### <span data-ttu-id="f063b-119">所有</span><span class="sxs-lookup"><span data-stu-id="f063b-119">None</span></span>
<span data-ttu-id="f063b-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f063b-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f063b-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f063b-121">OUTPUTS</span></span>

### <span data-ttu-id="f063b-122">PSAzureFirewallFqdnTag 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f063b-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="f063b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f063b-123">NOTES</span></span>

## <span data-ttu-id="f063b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f063b-124">RELATED LINKS</span></span>

[<span data-ttu-id="f063b-125">新-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f063b-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="f063b-126">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f063b-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
