---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 11f3a729c6818a7794a8b42a4b21a658530cc60d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911469"
---
# <span data-ttu-id="495f9-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="495f9-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="495f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="495f9-102">SYNOPSIS</span></span>
<span data-ttu-id="495f9-103">建立新對等 ASN</span><span class="sxs-lookup"><span data-stu-id="495f9-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="495f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="495f9-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495f9-105">描述</span><span class="sxs-lookup"><span data-stu-id="495f9-105">DESCRIPTION</span></span>
<span data-ttu-id="495f9-106">為訂閱建立新的 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="495f9-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="495f9-107">例子</span><span class="sxs-lookup"><span data-stu-id="495f9-107">EXAMPLES</span></span>

### <span data-ttu-id="495f9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="495f9-108">Example 1</span></span>
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

<span data-ttu-id="495f9-109">建立新對等體</span><span class="sxs-lookup"><span data-stu-id="495f9-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="495f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="495f9-110">PARAMETERS</span></span>

### <span data-ttu-id="495f9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="495f9-111">-AsJob</span></span>
<span data-ttu-id="495f9-112">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="495f9-112">Run in the background.</span></span>

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

### <span data-ttu-id="495f9-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="495f9-113">-ContactDetail</span></span>
<span data-ttu-id="495f9-114">如果問題通常是網路營運中心，用來聯繫的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="495f9-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="495f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495f9-115">-DefaultProfile</span></span>
<span data-ttu-id="495f9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="495f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495f9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="495f9-117">-Name</span></span>
<span data-ttu-id="495f9-118">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="495f9-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="495f9-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="495f9-119">-PeerAsn</span></span>
<span data-ttu-id="495f9-120">對等 Asn 資源識別碼。Get-AzPeerAsn來取回識別碼。</span><span class="sxs-lookup"><span data-stu-id="495f9-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="495f9-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="495f9-121">-PeerName</span></span>
<span data-ttu-id="495f9-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="495f9-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="495f9-123">-確認</span><span class="sxs-lookup"><span data-stu-id="495f9-123">-Confirm</span></span>
<span data-ttu-id="495f9-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="495f9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495f9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495f9-125">-WhatIf</span></span>
<span data-ttu-id="495f9-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="495f9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="495f9-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="495f9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495f9-128">CommonParameters</span></span>
<span data-ttu-id="495f9-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="495f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495f9-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="495f9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495f9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="495f9-131">INPUTS</span></span>

### <span data-ttu-id="495f9-132">沒有</span><span class="sxs-lookup"><span data-stu-id="495f9-132">None</span></span>

## <span data-ttu-id="495f9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="495f9-133">OUTPUTS</span></span>

### <span data-ttu-id="495f9-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="495f9-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="495f9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="495f9-135">NOTES</span></span>

## <span data-ttu-id="495f9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="495f9-136">RELATED LINKS</span></span>
