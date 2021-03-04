---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 2f1bdfd317a5578c5ce3a023f1c3cd0151026b80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911513"
---
# <span data-ttu-id="9b9ae-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="9b9ae-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="9b9ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9ae-103">用來將舊版對等資源轉換為 Azure 資源管理 (ARM) 資源。</span><span class="sxs-lookup"><span data-stu-id="9b9ae-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="9b9ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b9ae-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b9ae-105">描述</span><span class="sxs-lookup"><span data-stu-id="9b9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="9b9ae-106">該命令用來查看舊版對等資源，而您全部都將其轉換為 AZURE 資源管理 (ARM) 資源。</span><span class="sxs-lookup"><span data-stu-id="9b9ae-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="9b9ae-107">例子</span><span class="sxs-lookup"><span data-stu-id="9b9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="9b9ae-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9b9ae-108">Example 1</span></span>
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

<span data-ttu-id="9b9ae-109">獲得西雅圖的舊版對等互連</span><span class="sxs-lookup"><span data-stu-id="9b9ae-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="9b9ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b9ae-110">PARAMETERS</span></span>

### <span data-ttu-id="9b9ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b9ae-111">-DefaultProfile</span></span>
<span data-ttu-id="9b9ae-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b9ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b9ae-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="9b9ae-113">-Kind</span></span>
<span data-ttu-id="9b9ae-114">顯示所有對等資源 ，並按類型顯示。</span><span class="sxs-lookup"><span data-stu-id="9b9ae-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="9b9ae-115">-對等位置</span><span class="sxs-lookup"><span data-stu-id="9b9ae-115">-PeeringLocation</span></span>
<span data-ttu-id="9b9ae-116">顯示所有對等資源 ，並按類型顯示。</span><span class="sxs-lookup"><span data-stu-id="9b9ae-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="9b9ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9ae-117">CommonParameters</span></span>
<span data-ttu-id="9b9ae-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b9ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9ae-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b9ae-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9ae-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9b9ae-120">INPUTS</span></span>

### <span data-ttu-id="9b9ae-121">沒有</span><span class="sxs-lookup"><span data-stu-id="9b9ae-121">None</span></span>

## <span data-ttu-id="9b9ae-122">輸出</span><span class="sxs-lookup"><span data-stu-id="9b9ae-122">OUTPUTS</span></span>

### <span data-ttu-id="9b9ae-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9b9ae-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="9b9ae-124">筆記</span><span class="sxs-lookup"><span data-stu-id="9b9ae-124">NOTES</span></span>

## <span data-ttu-id="9b9ae-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b9ae-125">RELATED LINKS</span></span>
