---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288535"
---
# <span data-ttu-id="a62a2-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a62a2-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="a62a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a62a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a62a2-103">建立新的對等 ASN</span><span class="sxs-lookup"><span data-stu-id="a62a2-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="a62a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a62a2-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a62a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a62a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a62a2-106">為訂閱建立新的 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="a62a2-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="a62a2-107">示例</span><span class="sxs-lookup"><span data-stu-id="a62a2-107">EXAMPLES</span></span>

### <span data-ttu-id="a62a2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a62a2-108">Example 1</span></span>
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

<span data-ttu-id="a62a2-109">建立新的 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a62a2-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="a62a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a62a2-110">PARAMETERS</span></span>

### <span data-ttu-id="a62a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a62a2-111">-AsJob</span></span>
<span data-ttu-id="a62a2-112">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="a62a2-112">Run in the background.</span></span>

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

### <span data-ttu-id="a62a2-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="a62a2-113">-ContactDetail</span></span>
<span data-ttu-id="a62a2-114">當問題 arrise 通常是網路運營中心時，用來聯絡的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="a62a2-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="a62a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62a2-115">-DefaultProfile</span></span>
<span data-ttu-id="a62a2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a62a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a62a2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a62a2-117">-Name</span></span>
<span data-ttu-id="a62a2-118">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a62a2-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a62a2-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a62a2-119">-PeerAsn</span></span>
<span data-ttu-id="a62a2-120">對等 Asn 資源識別碼。使用 Get-AzPeerAsn 來檢索 Id。</span><span class="sxs-lookup"><span data-stu-id="a62a2-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="a62a2-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a62a2-121">-PeerName</span></span>
<span data-ttu-id="a62a2-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a62a2-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a62a2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a62a2-123">-Confirm</span></span>
<span data-ttu-id="a62a2-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a62a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a62a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a62a2-125">-WhatIf</span></span>
<span data-ttu-id="a62a2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a62a2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a62a2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a62a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a62a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62a2-128">CommonParameters</span></span>
<span data-ttu-id="a62a2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a62a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62a2-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a62a2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62a2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a62a2-131">INPUTS</span></span>

### <span data-ttu-id="a62a2-132">所有</span><span class="sxs-lookup"><span data-stu-id="a62a2-132">None</span></span>

## <span data-ttu-id="a62a2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a62a2-133">OUTPUTS</span></span>

### <span data-ttu-id="a62a2-134">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="a62a2-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a62a2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a62a2-135">NOTES</span></span>

## <span data-ttu-id="a62a2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a62a2-136">RELATED LINKS</span></span>
