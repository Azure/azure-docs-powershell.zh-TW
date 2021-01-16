---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280553"
---
# <span data-ttu-id="d6967-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="d6967-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="d6967-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6967-102">SYNOPSIS</span></span>
<span data-ttu-id="d6967-103">從父對等資源設定或更新已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="d6967-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="d6967-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6967-104">SYNTAX</span></span>

### <span data-ttu-id="d6967-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="d6967-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6967-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d6967-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6967-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6967-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6967-108">說明</span><span class="sxs-lookup"><span data-stu-id="d6967-108">DESCRIPTION</span></span>
<span data-ttu-id="d6967-109">允許從父對等資源更新已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="d6967-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="d6967-110">示例</span><span class="sxs-lookup"><span data-stu-id="d6967-110">EXAMPLES</span></span>

### <span data-ttu-id="d6967-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d6967-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="d6967-112">依資源識別碼更新 ASN。</span><span class="sxs-lookup"><span data-stu-id="d6967-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="d6967-113">參數</span><span class="sxs-lookup"><span data-stu-id="d6967-113">PARAMETERS</span></span>

### <span data-ttu-id="d6967-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6967-114">-AsJob</span></span>
<span data-ttu-id="d6967-115">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="d6967-115">Run in the background.</span></span>

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

### <span data-ttu-id="d6967-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="d6967-116">-Asn</span></span>
<span data-ttu-id="d6967-117">要註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="d6967-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6967-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6967-118">-DefaultProfile</span></span>
<span data-ttu-id="d6967-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6967-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6967-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6967-120">-InputObject</span></span>
<span data-ttu-id="d6967-121">使用 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d6967-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6967-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6967-122">-Name</span></span>
<span data-ttu-id="d6967-123">要註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="d6967-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6967-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d6967-124">-PeeringName</span></span>
<span data-ttu-id="d6967-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d6967-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6967-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6967-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6967-127">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d6967-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6967-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6967-128">-ResourceId</span></span>
<span data-ttu-id="d6967-129">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="d6967-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6967-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d6967-130">-Confirm</span></span>
<span data-ttu-id="d6967-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6967-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6967-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6967-132">-WhatIf</span></span>
<span data-ttu-id="d6967-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6967-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6967-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6967-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6967-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6967-135">CommonParameters</span></span>
<span data-ttu-id="d6967-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6967-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6967-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6967-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6967-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d6967-138">INPUTS</span></span>

### <span data-ttu-id="d6967-139">PSPeeringRegisteredAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="d6967-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="d6967-140">System.object</span><span class="sxs-lookup"><span data-stu-id="d6967-140">System.String</span></span>

## <span data-ttu-id="d6967-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d6967-141">OUTPUTS</span></span>

### <span data-ttu-id="d6967-142">PSPeeringRegisteredAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="d6967-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="d6967-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d6967-143">NOTES</span></span>

## <span data-ttu-id="d6967-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6967-144">RELATED LINKS</span></span>
