---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288479"
---
# <span data-ttu-id="95211-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="95211-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="95211-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95211-102">SYNOPSIS</span></span>
<span data-ttu-id="95211-103">更新連絡人資訊</span><span class="sxs-lookup"><span data-stu-id="95211-103">Update Contact Information</span></span>

## <span data-ttu-id="95211-104">句法</span><span class="sxs-lookup"><span data-stu-id="95211-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95211-105">說明</span><span class="sxs-lookup"><span data-stu-id="95211-105">DESCRIPTION</span></span>
<span data-ttu-id="95211-106">可讓您更新訂閱上 PeerAsn 的連絡人資訊。</span><span class="sxs-lookup"><span data-stu-id="95211-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="95211-107">示例</span><span class="sxs-lookup"><span data-stu-id="95211-107">EXAMPLES</span></span>

### <span data-ttu-id="95211-108">範例1</span><span class="sxs-lookup"><span data-stu-id="95211-108">Example 1</span></span>
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

<span data-ttu-id="95211-109">將電子郵件地址新增至對等 Asn</span><span class="sxs-lookup"><span data-stu-id="95211-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="95211-110">參數</span><span class="sxs-lookup"><span data-stu-id="95211-110">PARAMETERS</span></span>

### <span data-ttu-id="95211-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95211-111">-AsJob</span></span>
<span data-ttu-id="95211-112">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="95211-112">Run in the background.</span></span>

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

### <span data-ttu-id="95211-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95211-113">-DefaultProfile</span></span>
<span data-ttu-id="95211-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95211-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95211-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95211-115">-InputObject</span></span>
<span data-ttu-id="95211-116">{{Fill InputObject 描述}}</span><span class="sxs-lookup"><span data-stu-id="95211-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="95211-117">-確認</span><span class="sxs-lookup"><span data-stu-id="95211-117">-Confirm</span></span>
<span data-ttu-id="95211-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95211-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95211-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95211-119">-WhatIf</span></span>
<span data-ttu-id="95211-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95211-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95211-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95211-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95211-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95211-122">CommonParameters</span></span>
<span data-ttu-id="95211-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95211-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95211-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95211-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95211-125">輸入</span><span class="sxs-lookup"><span data-stu-id="95211-125">INPUTS</span></span>

### <span data-ttu-id="95211-126">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="95211-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="95211-127">輸出</span><span class="sxs-lookup"><span data-stu-id="95211-127">OUTPUTS</span></span>

### <span data-ttu-id="95211-128">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="95211-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="95211-129">筆記</span><span class="sxs-lookup"><span data-stu-id="95211-129">NOTES</span></span>

## <span data-ttu-id="95211-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="95211-130">RELATED LINKS</span></span>
