---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286468"
---
# <span data-ttu-id="703e2-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="703e2-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="703e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="703e2-102">SYNOPSIS</span></span>
<span data-ttu-id="703e2-103">用來將舊版對等資源轉換為 Azure 資源管理 (ARM) 資源。</span><span class="sxs-lookup"><span data-stu-id="703e2-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="703e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="703e2-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="703e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="703e2-105">DESCRIPTION</span></span>
<span data-ttu-id="703e2-106">此命令是用來查看舊版對等資源，您可以將它們轉換成 Azure 資源管理 (ARM) 資源。</span><span class="sxs-lookup"><span data-stu-id="703e2-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="703e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="703e2-107">EXAMPLES</span></span>

### <span data-ttu-id="703e2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="703e2-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="703e2-109">取得西雅圖的舊版對等</span><span class="sxs-lookup"><span data-stu-id="703e2-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="703e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="703e2-110">PARAMETERS</span></span>

### <span data-ttu-id="703e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703e2-111">-DefaultProfile</span></span>
<span data-ttu-id="703e2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="703e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="703e2-113">類型</span><span class="sxs-lookup"><span data-stu-id="703e2-113">-Kind</span></span>
<span data-ttu-id="703e2-114">依類型顯示所有對等資源。</span><span class="sxs-lookup"><span data-stu-id="703e2-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703e2-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="703e2-115">-PeeringLocation</span></span>
<span data-ttu-id="703e2-116">依類型顯示所有對等資源。</span><span class="sxs-lookup"><span data-stu-id="703e2-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703e2-117">CommonParameters</span></span>
<span data-ttu-id="703e2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="703e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703e2-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="703e2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703e2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="703e2-120">INPUTS</span></span>

### <span data-ttu-id="703e2-121">所有</span><span class="sxs-lookup"><span data-stu-id="703e2-121">None</span></span>

## <span data-ttu-id="703e2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="703e2-122">OUTPUTS</span></span>

### <span data-ttu-id="703e2-123">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="703e2-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="703e2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="703e2-124">NOTES</span></span>

## <span data-ttu-id="703e2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="703e2-125">RELATED LINKS</span></span>
