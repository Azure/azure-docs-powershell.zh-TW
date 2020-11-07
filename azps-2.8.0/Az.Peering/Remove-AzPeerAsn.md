---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791724"
---
# <span data-ttu-id="239a4-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="239a4-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="239a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="239a4-102">SYNOPSIS</span></span>
<span data-ttu-id="239a4-103">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="239a4-103">Remove Peer Asn</span></span>

## <span data-ttu-id="239a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="239a4-104">SYNTAX</span></span>

### <span data-ttu-id="239a4-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="239a4-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239a4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="239a4-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="239a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="239a4-107">DESCRIPTION</span></span>
<span data-ttu-id="239a4-108">從訂閱中移除 PeerAsn。</span><span class="sxs-lookup"><span data-stu-id="239a4-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="239a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="239a4-109">EXAMPLES</span></span>

### <span data-ttu-id="239a4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="239a4-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="239a4-111">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="239a4-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="239a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="239a4-112">PARAMETERS</span></span>

### <span data-ttu-id="239a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="239a4-113">-AsJob</span></span>
<span data-ttu-id="239a4-114">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="239a4-114">Run in the background.</span></span>

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

### <span data-ttu-id="239a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239a4-115">-DefaultProfile</span></span>
<span data-ttu-id="239a4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="239a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="239a4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="239a4-117">-Force</span></span>
<span data-ttu-id="239a4-118">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="239a4-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="239a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="239a4-119">-InputObject</span></span>
<span data-ttu-id="239a4-120">PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="239a4-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="239a4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="239a4-121">-Name</span></span>
<span data-ttu-id="239a4-122">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="239a4-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="239a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="239a4-123">-PassThru</span></span>
<span data-ttu-id="239a4-124">如果完成，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="239a4-124">Return true if complete</span></span>

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

### <span data-ttu-id="239a4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="239a4-125">-Confirm</span></span>
<span data-ttu-id="239a4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="239a4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="239a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="239a4-127">-WhatIf</span></span>
<span data-ttu-id="239a4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="239a4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="239a4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="239a4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="239a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239a4-130">CommonParameters</span></span>
<span data-ttu-id="239a4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="239a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239a4-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="239a4-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239a4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="239a4-133">INPUTS</span></span>

### <span data-ttu-id="239a4-134">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="239a4-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="239a4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="239a4-135">OUTPUTS</span></span>

### <span data-ttu-id="239a4-136">System.object</span><span class="sxs-lookup"><span data-stu-id="239a4-136">System.Boolean</span></span>

## <span data-ttu-id="239a4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="239a4-137">NOTES</span></span>

## <span data-ttu-id="239a4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="239a4-138">RELATED LINKS</span></span>
