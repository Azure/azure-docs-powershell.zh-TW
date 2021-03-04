---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: fd4058cd09ad0d0ca27f8324368cd6d0277cec7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911405"
---
# <span data-ttu-id="316a2-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="316a2-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="316a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="316a2-102">SYNOPSIS</span></span>
<span data-ttu-id="316a2-103">更新連絡人資訊</span><span class="sxs-lookup"><span data-stu-id="316a2-103">Update Contact Information</span></span>

## <span data-ttu-id="316a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="316a2-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316a2-105">描述</span><span class="sxs-lookup"><span data-stu-id="316a2-105">DESCRIPTION</span></span>
<span data-ttu-id="316a2-106">可讓您更新訂閱上的 PeerAsn 連絡人資訊。</span><span class="sxs-lookup"><span data-stu-id="316a2-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="316a2-107">例子</span><span class="sxs-lookup"><span data-stu-id="316a2-107">EXAMPLES</span></span>

### <span data-ttu-id="316a2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="316a2-108">Example 1</span></span>
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

<span data-ttu-id="316a2-109">將電子郵件地址新增到對等 Asn</span><span class="sxs-lookup"><span data-stu-id="316a2-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="316a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="316a2-110">PARAMETERS</span></span>

### <span data-ttu-id="316a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="316a2-111">-AsJob</span></span>
<span data-ttu-id="316a2-112">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="316a2-112">Run in the background.</span></span>

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

### <span data-ttu-id="316a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316a2-113">-DefaultProfile</span></span>
<span data-ttu-id="316a2-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="316a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316a2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="316a2-115">-InputObject</span></span>
<span data-ttu-id="316a2-116">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="316a2-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="316a2-117">-確認</span><span class="sxs-lookup"><span data-stu-id="316a2-117">-Confirm</span></span>
<span data-ttu-id="316a2-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="316a2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316a2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316a2-119">-WhatIf</span></span>
<span data-ttu-id="316a2-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="316a2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="316a2-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="316a2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316a2-122">CommonParameters</span></span>
<span data-ttu-id="316a2-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="316a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316a2-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="316a2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316a2-125">輸入</span><span class="sxs-lookup"><span data-stu-id="316a2-125">INPUTS</span></span>

### <span data-ttu-id="316a2-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="316a2-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="316a2-127">輸出</span><span class="sxs-lookup"><span data-stu-id="316a2-127">OUTPUTS</span></span>

### <span data-ttu-id="316a2-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="316a2-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="316a2-129">筆記</span><span class="sxs-lookup"><span data-stu-id="316a2-129">NOTES</span></span>

## <span data-ttu-id="316a2-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="316a2-130">RELATED LINKS</span></span>
