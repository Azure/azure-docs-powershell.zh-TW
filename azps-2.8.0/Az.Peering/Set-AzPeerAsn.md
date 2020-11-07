---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791720"
---
# <span data-ttu-id="ad83c-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ad83c-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="ad83c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad83c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad83c-103">更新連絡人資訊</span><span class="sxs-lookup"><span data-stu-id="ad83c-103">Update Contact Information</span></span>

## <span data-ttu-id="ad83c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad83c-104">SYNTAX</span></span>

### <span data-ttu-id="ad83c-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="ad83c-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad83c-106">設置</span><span class="sxs-lookup"><span data-stu-id="ad83c-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad83c-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad83c-107">DESCRIPTION</span></span>
<span data-ttu-id="ad83c-108">可讓您更新訂閱上 PeerAsn 的連絡人資訊。</span><span class="sxs-lookup"><span data-stu-id="ad83c-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="ad83c-109">示例</span><span class="sxs-lookup"><span data-stu-id="ad83c-109">EXAMPLES</span></span>

### <span data-ttu-id="ad83c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ad83c-110">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="ad83c-111">將電子郵件地址新增至對等 Asn</span><span class="sxs-lookup"><span data-stu-id="ad83c-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="ad83c-112">參數</span><span class="sxs-lookup"><span data-stu-id="ad83c-112">PARAMETERS</span></span>

### <span data-ttu-id="ad83c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad83c-113">-AsJob</span></span>
<span data-ttu-id="ad83c-114">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="ad83c-114">Run in the background.</span></span>

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

### <span data-ttu-id="ad83c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad83c-115">-DefaultProfile</span></span>
<span data-ttu-id="ad83c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad83c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad83c-117">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="ad83c-117">-Email</span></span>
<span data-ttu-id="ad83c-118">電子郵件</span><span class="sxs-lookup"><span data-stu-id="ad83c-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad83c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad83c-119">-InputObject</span></span>
<span data-ttu-id="ad83c-120">{{Fill InputObject 描述}}</span><span class="sxs-lookup"><span data-stu-id="ad83c-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad83c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad83c-121">-Name</span></span>
<span data-ttu-id="ad83c-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="ad83c-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad83c-123">-電話</span><span class="sxs-lookup"><span data-stu-id="ad83c-123">-Phone</span></span>
<span data-ttu-id="ad83c-124">電話</span><span class="sxs-lookup"><span data-stu-id="ad83c-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad83c-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ad83c-125">-Confirm</span></span>
<span data-ttu-id="ad83c-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad83c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad83c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad83c-127">-WhatIf</span></span>
<span data-ttu-id="ad83c-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad83c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad83c-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad83c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad83c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad83c-130">CommonParameters</span></span>
<span data-ttu-id="ad83c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad83c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad83c-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad83c-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad83c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ad83c-133">INPUTS</span></span>

### <span data-ttu-id="ad83c-134">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="ad83c-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ad83c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ad83c-135">OUTPUTS</span></span>

### <span data-ttu-id="ad83c-136">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="ad83c-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ad83c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ad83c-137">NOTES</span></span>

## <span data-ttu-id="ad83c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad83c-138">RELATED LINKS</span></span>
