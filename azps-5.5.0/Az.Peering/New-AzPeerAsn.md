---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131038"
---
# <span data-ttu-id="87ce0-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="87ce0-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="87ce0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="87ce0-103">建立新的對等 ASN</span><span class="sxs-lookup"><span data-stu-id="87ce0-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="87ce0-104">句法</span><span class="sxs-lookup"><span data-stu-id="87ce0-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ce0-105">說明</span><span class="sxs-lookup"><span data-stu-id="87ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="87ce0-106">為訂閱建立新的 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="87ce0-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="87ce0-107">示例</span><span class="sxs-lookup"><span data-stu-id="87ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="87ce0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="87ce0-108">Example 1</span></span>
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

<span data-ttu-id="87ce0-109">建立新的 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="87ce0-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="87ce0-110">參數</span><span class="sxs-lookup"><span data-stu-id="87ce0-110">PARAMETERS</span></span>

### <span data-ttu-id="87ce0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87ce0-111">-AsJob</span></span>
<span data-ttu-id="87ce0-112">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="87ce0-112">Run in the background.</span></span>

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

### <span data-ttu-id="87ce0-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="87ce0-113">-ContactDetail</span></span>
<span data-ttu-id="87ce0-114">當問題 arrise 通常是網路運營中心時，用來聯絡的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="87ce0-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="87ce0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ce0-115">-DefaultProfile</span></span>
<span data-ttu-id="87ce0-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87ce0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87ce0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="87ce0-117">-Name</span></span>
<span data-ttu-id="87ce0-118">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="87ce0-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="87ce0-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="87ce0-119">-PeerAsn</span></span>
<span data-ttu-id="87ce0-120">對等 Asn 資源識別碼。使用 Get-AzPeerAsn 來檢索 Id。</span><span class="sxs-lookup"><span data-stu-id="87ce0-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="87ce0-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="87ce0-121">-PeerName</span></span>
<span data-ttu-id="87ce0-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="87ce0-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="87ce0-123">-確認</span><span class="sxs-lookup"><span data-stu-id="87ce0-123">-Confirm</span></span>
<span data-ttu-id="87ce0-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87ce0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87ce0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87ce0-125">-WhatIf</span></span>
<span data-ttu-id="87ce0-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87ce0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87ce0-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87ce0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87ce0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ce0-128">CommonParameters</span></span>
<span data-ttu-id="87ce0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87ce0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ce0-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="87ce0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ce0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="87ce0-131">INPUTS</span></span>

### <span data-ttu-id="87ce0-132">所有</span><span class="sxs-lookup"><span data-stu-id="87ce0-132">None</span></span>

## <span data-ttu-id="87ce0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="87ce0-133">OUTPUTS</span></span>

### <span data-ttu-id="87ce0-134">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="87ce0-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="87ce0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="87ce0-135">NOTES</span></span>

## <span data-ttu-id="87ce0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="87ce0-136">RELATED LINKS</span></span>
