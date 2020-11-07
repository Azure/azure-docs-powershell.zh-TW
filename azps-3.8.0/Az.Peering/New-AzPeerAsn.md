---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: f811f73b50f88a256de62069a287d113607e7ee1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965921"
---
# <span data-ttu-id="4f766-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="4f766-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="4f766-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f766-102">SYNOPSIS</span></span>
<span data-ttu-id="4f766-103">建立新的對等 ASN</span><span class="sxs-lookup"><span data-stu-id="4f766-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="4f766-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f766-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f766-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f766-105">DESCRIPTION</span></span>
<span data-ttu-id="4f766-106">為訂閱建立新的 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="4f766-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="4f766-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f766-107">EXAMPLES</span></span>

### <span data-ttu-id="4f766-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4f766-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="4f766-109">建立新的 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="4f766-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="4f766-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f766-110">PARAMETERS</span></span>

### <span data-ttu-id="4f766-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f766-111">-AsJob</span></span>
<span data-ttu-id="4f766-112">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="4f766-112">Run in the background.</span></span>

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

### <span data-ttu-id="4f766-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f766-113">-DefaultProfile</span></span>
<span data-ttu-id="4f766-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f766-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f766-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="4f766-115">-Email</span></span>
<span data-ttu-id="4f766-116">電子郵件</span><span class="sxs-lookup"><span data-stu-id="4f766-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f766-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f766-117">-Name</span></span>
<span data-ttu-id="4f766-118">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="4f766-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4f766-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="4f766-119">-PeerAsn</span></span>
<span data-ttu-id="4f766-120">對等 Asn 資源識別碼。使用 Get-AzPeerAsn 來檢索 Id。</span><span class="sxs-lookup"><span data-stu-id="4f766-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f766-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="4f766-121">-PeerName</span></span>
<span data-ttu-id="4f766-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="4f766-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4f766-123">-電話</span><span class="sxs-lookup"><span data-stu-id="4f766-123">-Phone</span></span>
<span data-ttu-id="4f766-124">電話</span><span class="sxs-lookup"><span data-stu-id="4f766-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f766-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4f766-125">-Confirm</span></span>
<span data-ttu-id="4f766-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f766-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f766-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f766-127">-WhatIf</span></span>
<span data-ttu-id="4f766-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f766-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f766-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f766-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f766-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f766-130">CommonParameters</span></span>
<span data-ttu-id="4f766-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f766-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f766-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f766-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f766-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4f766-133">INPUTS</span></span>

### <span data-ttu-id="4f766-134">所有</span><span class="sxs-lookup"><span data-stu-id="4f766-134">None</span></span>

## <span data-ttu-id="4f766-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4f766-135">OUTPUTS</span></span>

### <span data-ttu-id="4f766-136">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="4f766-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="4f766-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4f766-137">NOTES</span></span>

## <span data-ttu-id="4f766-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f766-138">RELATED LINKS</span></span>
