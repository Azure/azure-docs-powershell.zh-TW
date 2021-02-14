---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134746"
---
# <span data-ttu-id="a6455-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a6455-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="a6455-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6455-102">SYNOPSIS</span></span>
<span data-ttu-id="a6455-103">從 ARM 取得 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="a6455-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="a6455-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6455-104">SYNTAX</span></span>

### <span data-ttu-id="a6455-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a6455-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6455-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6455-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6455-107">說明</span><span class="sxs-lookup"><span data-stu-id="a6455-107">DESCRIPTION</span></span>
<span data-ttu-id="a6455-108">取得訂閱的 PeerAsn。</span><span class="sxs-lookup"><span data-stu-id="a6455-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="a6455-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6455-109">EXAMPLES</span></span>

### <span data-ttu-id="a6455-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a6455-110">Example 1</span></span>
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

<span data-ttu-id="a6455-111">取得 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a6455-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="a6455-112">參數</span><span class="sxs-lookup"><span data-stu-id="a6455-112">PARAMETERS</span></span>

### <span data-ttu-id="a6455-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6455-113">-DefaultProfile</span></span>
<span data-ttu-id="a6455-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6455-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6455-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6455-115">-Name</span></span>
<span data-ttu-id="a6455-116">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a6455-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a6455-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6455-117">-ResourceId</span></span>
<span data-ttu-id="a6455-118">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="a6455-118">The resource id string name.</span></span>

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

### <span data-ttu-id="a6455-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6455-119">CommonParameters</span></span>
<span data-ttu-id="a6455-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6455-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6455-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a6455-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6455-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a6455-122">INPUTS</span></span>

### <span data-ttu-id="a6455-123">System.object</span><span class="sxs-lookup"><span data-stu-id="a6455-123">System.String</span></span>

## <span data-ttu-id="a6455-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a6455-124">OUTPUTS</span></span>

### <span data-ttu-id="a6455-125">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="a6455-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a6455-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a6455-126">NOTES</span></span>

## <span data-ttu-id="a6455-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6455-127">RELATED LINKS</span></span>
