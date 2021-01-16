---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288500"
---
# <span data-ttu-id="4016a-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="4016a-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="4016a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4016a-102">SYNOPSIS</span></span>
<span data-ttu-id="4016a-103">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="4016a-103">Remove Peer Asn</span></span>

## <span data-ttu-id="4016a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4016a-104">SYNTAX</span></span>

### <span data-ttu-id="4016a-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="4016a-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4016a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4016a-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4016a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4016a-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4016a-108">說明</span><span class="sxs-lookup"><span data-stu-id="4016a-108">DESCRIPTION</span></span>
<span data-ttu-id="4016a-109">從訂閱中移除 PeerAsn。</span><span class="sxs-lookup"><span data-stu-id="4016a-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="4016a-110">示例</span><span class="sxs-lookup"><span data-stu-id="4016a-110">EXAMPLES</span></span>

### <span data-ttu-id="4016a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4016a-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="4016a-112">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="4016a-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="4016a-113">參數</span><span class="sxs-lookup"><span data-stu-id="4016a-113">PARAMETERS</span></span>

### <span data-ttu-id="4016a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4016a-114">-AsJob</span></span>
<span data-ttu-id="4016a-115">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="4016a-115">Run in the background.</span></span>

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

### <span data-ttu-id="4016a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4016a-116">-DefaultProfile</span></span>
<span data-ttu-id="4016a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4016a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4016a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4016a-118">-Force</span></span>
<span data-ttu-id="4016a-119">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="4016a-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="4016a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4016a-120">-InputObject</span></span>
<span data-ttu-id="4016a-121">PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="4016a-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4016a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4016a-122">-Name</span></span>
<span data-ttu-id="4016a-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="4016a-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4016a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4016a-124">-PassThru</span></span>
<span data-ttu-id="4016a-125">如果完成，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="4016a-125">Return true if complete</span></span>

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

### <span data-ttu-id="4016a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4016a-126">-ResourceId</span></span>
<span data-ttu-id="4016a-127">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="4016a-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4016a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4016a-128">-Confirm</span></span>
<span data-ttu-id="4016a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4016a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4016a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4016a-130">-WhatIf</span></span>
<span data-ttu-id="4016a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4016a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4016a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4016a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4016a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4016a-133">CommonParameters</span></span>
<span data-ttu-id="4016a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4016a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4016a-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4016a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4016a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4016a-136">INPUTS</span></span>

### <span data-ttu-id="4016a-137">PSPeerAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="4016a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="4016a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="4016a-138">System.String</span></span>

## <span data-ttu-id="4016a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4016a-139">OUTPUTS</span></span>

### <span data-ttu-id="4016a-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4016a-140">System.Boolean</span></span>

## <span data-ttu-id="4016a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4016a-141">NOTES</span></span>

## <span data-ttu-id="4016a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4016a-142">RELATED LINKS</span></span>
