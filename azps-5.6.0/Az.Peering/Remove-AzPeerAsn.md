---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911430"
---
# <span data-ttu-id="48ad5-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="48ad5-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="48ad5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="48ad5-103">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="48ad5-103">Remove Peer Asn</span></span>

## <span data-ttu-id="48ad5-104">語法</span><span class="sxs-lookup"><span data-stu-id="48ad5-104">SYNTAX</span></span>

### <span data-ttu-id="48ad5-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="48ad5-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ad5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48ad5-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ad5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="48ad5-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48ad5-108">描述</span><span class="sxs-lookup"><span data-stu-id="48ad5-108">DESCRIPTION</span></span>
<span data-ttu-id="48ad5-109">從訂閱移除對等體。</span><span class="sxs-lookup"><span data-stu-id="48ad5-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="48ad5-110">例子</span><span class="sxs-lookup"><span data-stu-id="48ad5-110">EXAMPLES</span></span>

### <span data-ttu-id="48ad5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="48ad5-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="48ad5-112">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="48ad5-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="48ad5-113">參數</span><span class="sxs-lookup"><span data-stu-id="48ad5-113">PARAMETERS</span></span>

### <span data-ttu-id="48ad5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48ad5-114">-AsJob</span></span>
<span data-ttu-id="48ad5-115">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="48ad5-115">Run in the background.</span></span>

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

### <span data-ttu-id="48ad5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ad5-116">-DefaultProfile</span></span>
<span data-ttu-id="48ad5-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="48ad5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ad5-118">-強制</span><span class="sxs-lookup"><span data-stu-id="48ad5-118">-Force</span></span>
<span data-ttu-id="48ad5-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="48ad5-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="48ad5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48ad5-120">-InputObject</span></span>
<span data-ttu-id="48ad5-121">對等物件。</span><span class="sxs-lookup"><span data-stu-id="48ad5-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="48ad5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="48ad5-122">-Name</span></span>
<span data-ttu-id="48ad5-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="48ad5-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="48ad5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48ad5-124">-PassThru</span></span>
<span data-ttu-id="48ad5-125">如果已完成，請返回 True</span><span class="sxs-lookup"><span data-stu-id="48ad5-125">Return true if complete</span></span>

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

### <span data-ttu-id="48ad5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48ad5-126">-ResourceId</span></span>
<span data-ttu-id="48ad5-127">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="48ad5-127">The resource id string name.</span></span>

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

### <span data-ttu-id="48ad5-128">-確認</span><span class="sxs-lookup"><span data-stu-id="48ad5-128">-Confirm</span></span>
<span data-ttu-id="48ad5-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="48ad5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ad5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ad5-130">-WhatIf</span></span>
<span data-ttu-id="48ad5-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48ad5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48ad5-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48ad5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ad5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ad5-133">CommonParameters</span></span>
<span data-ttu-id="48ad5-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48ad5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ad5-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48ad5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ad5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="48ad5-136">INPUTS</span></span>

### <span data-ttu-id="48ad5-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="48ad5-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="48ad5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="48ad5-138">System.String</span></span>

## <span data-ttu-id="48ad5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="48ad5-139">OUTPUTS</span></span>

### <span data-ttu-id="48ad5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48ad5-140">System.Boolean</span></span>

## <span data-ttu-id="48ad5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="48ad5-141">NOTES</span></span>

## <span data-ttu-id="48ad5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="48ad5-142">RELATED LINKS</span></span>
