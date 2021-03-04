---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 9498183e66a0991f7a724065bb5a88e954cd6594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911510"
---
# <span data-ttu-id="3bee6-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="3bee6-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="3bee6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3bee6-102">SYNOPSIS</span></span>
<span data-ttu-id="3bee6-103">從 ARM 中獲得對等物件。</span><span class="sxs-lookup"><span data-stu-id="3bee6-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="3bee6-104">語法</span><span class="sxs-lookup"><span data-stu-id="3bee6-104">SYNTAX</span></span>

### <span data-ttu-id="3bee6-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3bee6-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bee6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3bee6-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bee6-107">描述</span><span class="sxs-lookup"><span data-stu-id="3bee6-107">DESCRIPTION</span></span>
<span data-ttu-id="3bee6-108">獲得訂閱的對等體。</span><span class="sxs-lookup"><span data-stu-id="3bee6-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="3bee6-109">例子</span><span class="sxs-lookup"><span data-stu-id="3bee6-109">EXAMPLES</span></span>

### <span data-ttu-id="3bee6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3bee6-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="3bee6-111">獲得對等體</span><span class="sxs-lookup"><span data-stu-id="3bee6-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="3bee6-112">參數</span><span class="sxs-lookup"><span data-stu-id="3bee6-112">PARAMETERS</span></span>

### <span data-ttu-id="3bee6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bee6-113">-DefaultProfile</span></span>
<span data-ttu-id="3bee6-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bee6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bee6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bee6-115">-Name</span></span>
<span data-ttu-id="3bee6-116">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="3bee6-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bee6-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bee6-117">-ResourceId</span></span>
<span data-ttu-id="3bee6-118">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="3bee6-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bee6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bee6-119">CommonParameters</span></span>
<span data-ttu-id="3bee6-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3bee6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bee6-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bee6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bee6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3bee6-122">INPUTS</span></span>

### <span data-ttu-id="3bee6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3bee6-123">System.String</span></span>

## <span data-ttu-id="3bee6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3bee6-124">OUTPUTS</span></span>

### <span data-ttu-id="3bee6-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="3bee6-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="3bee6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3bee6-126">NOTES</span></span>

## <span data-ttu-id="3bee6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bee6-127">RELATED LINKS</span></span>
