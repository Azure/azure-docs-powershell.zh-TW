---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126308"
---
# <span data-ttu-id="5df17-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="5df17-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="5df17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5df17-102">SYNOPSIS</span></span>
<span data-ttu-id="5df17-103">建立新的對等 ASN</span><span class="sxs-lookup"><span data-stu-id="5df17-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="5df17-104">句法</span><span class="sxs-lookup"><span data-stu-id="5df17-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df17-105">說明</span><span class="sxs-lookup"><span data-stu-id="5df17-105">DESCRIPTION</span></span>
<span data-ttu-id="5df17-106">為訂閱建立新的 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="5df17-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="5df17-107">示例</span><span class="sxs-lookup"><span data-stu-id="5df17-107">EXAMPLES</span></span>

### <span data-ttu-id="5df17-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5df17-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="5df17-109">建立新的 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="5df17-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="5df17-110">參數</span><span class="sxs-lookup"><span data-stu-id="5df17-110">PARAMETERS</span></span>

### <span data-ttu-id="5df17-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5df17-111">-AsJob</span></span>
<span data-ttu-id="5df17-112">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="5df17-112">Run in the background.</span></span>

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

### <span data-ttu-id="5df17-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="5df17-113">-ContactDetail</span></span>
<span data-ttu-id="5df17-114">當問題 arrise 通常是網路運營中心時，用來聯絡的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="5df17-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df17-115">-DefaultProfile</span></span>
<span data-ttu-id="5df17-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5df17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df17-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5df17-117">-Name</span></span>
<span data-ttu-id="5df17-118">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="5df17-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5df17-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="5df17-119">-PeerAsn</span></span>
<span data-ttu-id="5df17-120">對等 Asn 資源識別碼。使用 Get-AzPeerAsn 來檢索 Id。</span><span class="sxs-lookup"><span data-stu-id="5df17-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="5df17-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="5df17-121">-PeerName</span></span>
<span data-ttu-id="5df17-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="5df17-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5df17-123">-確認</span><span class="sxs-lookup"><span data-stu-id="5df17-123">-Confirm</span></span>
<span data-ttu-id="5df17-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5df17-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df17-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df17-125">-WhatIf</span></span>
<span data-ttu-id="5df17-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5df17-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5df17-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5df17-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df17-128">CommonParameters</span></span>
<span data-ttu-id="5df17-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5df17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df17-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5df17-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df17-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5df17-131">INPUTS</span></span>

### <span data-ttu-id="5df17-132">所有</span><span class="sxs-lookup"><span data-stu-id="5df17-132">None</span></span>

## <span data-ttu-id="5df17-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5df17-133">OUTPUTS</span></span>

### <span data-ttu-id="5df17-134">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="5df17-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="5df17-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5df17-135">NOTES</span></span>

## <span data-ttu-id="5df17-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5df17-136">RELATED LINKS</span></span>