---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 559d2d8c069d7e36630600d0fcdc16ea475da9f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965937"
---
# <span data-ttu-id="d842f-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d842f-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="d842f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d842f-102">SYNOPSIS</span></span>
<span data-ttu-id="d842f-103">從 ARM 取得 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="d842f-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="d842f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d842f-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d842f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d842f-105">DESCRIPTION</span></span>
<span data-ttu-id="d842f-106">取得訂閱的 PeerAsn。</span><span class="sxs-lookup"><span data-stu-id="d842f-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="d842f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d842f-107">EXAMPLES</span></span>

### <span data-ttu-id="d842f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d842f-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="d842f-109">取得 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="d842f-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="d842f-110">參數</span><span class="sxs-lookup"><span data-stu-id="d842f-110">PARAMETERS</span></span>

### <span data-ttu-id="d842f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d842f-111">-DefaultProfile</span></span>
<span data-ttu-id="d842f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d842f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d842f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d842f-113">-Name</span></span>
<span data-ttu-id="d842f-114">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d842f-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d842f-115">CommonParameters</span></span>
<span data-ttu-id="d842f-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d842f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d842f-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d842f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d842f-118">輸入</span><span class="sxs-lookup"><span data-stu-id="d842f-118">INPUTS</span></span>

### <span data-ttu-id="d842f-119">所有</span><span class="sxs-lookup"><span data-stu-id="d842f-119">None</span></span>

## <span data-ttu-id="d842f-120">輸出</span><span class="sxs-lookup"><span data-stu-id="d842f-120">OUTPUTS</span></span>

### <span data-ttu-id="d842f-121">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="d842f-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="d842f-122">筆記</span><span class="sxs-lookup"><span data-stu-id="d842f-122">NOTES</span></span>

## <span data-ttu-id="d842f-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="d842f-123">RELATED LINKS</span></span>
