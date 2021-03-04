---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: b4533497c1be0fd42e70cc0b7636aa2d4d5a7a98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911397"
---
# <span data-ttu-id="30339-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="30339-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="30339-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30339-102">SYNOPSIS</span></span>
<span data-ttu-id="30339-103">從父對等資源設定或更新已登錄的 ASN。</span><span class="sxs-lookup"><span data-stu-id="30339-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="30339-104">語法</span><span class="sxs-lookup"><span data-stu-id="30339-104">SYNTAX</span></span>

### <span data-ttu-id="30339-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="30339-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30339-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="30339-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30339-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30339-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30339-108">描述</span><span class="sxs-lookup"><span data-stu-id="30339-108">DESCRIPTION</span></span>
<span data-ttu-id="30339-109">允許從父對等資源更新登錄的 ASN。</span><span class="sxs-lookup"><span data-stu-id="30339-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="30339-110">例子</span><span class="sxs-lookup"><span data-stu-id="30339-110">EXAMPLES</span></span>

### <span data-ttu-id="30339-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="30339-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="30339-112">根據資源識別碼更新 ASN。</span><span class="sxs-lookup"><span data-stu-id="30339-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="30339-113">參數</span><span class="sxs-lookup"><span data-stu-id="30339-113">PARAMETERS</span></span>

### <span data-ttu-id="30339-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30339-114">-AsJob</span></span>
<span data-ttu-id="30339-115">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="30339-115">Run in the background.</span></span>

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

### <span data-ttu-id="30339-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="30339-116">-Asn</span></span>
<span data-ttu-id="30339-117">要註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="30339-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="30339-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30339-118">-DefaultProfile</span></span>
<span data-ttu-id="30339-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30339-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30339-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30339-120">-InputObject</span></span>
<span data-ttu-id="30339-121">使用Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="30339-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="30339-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="30339-122">-Name</span></span>
<span data-ttu-id="30339-123">要註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="30339-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="30339-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="30339-124">-PeeringName</span></span>
<span data-ttu-id="30339-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="30339-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="30339-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30339-126">-ResourceGroupName</span></span>
<span data-ttu-id="30339-127">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="30339-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="30339-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30339-128">-ResourceId</span></span>
<span data-ttu-id="30339-129">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="30339-129">The resource id string name.</span></span>

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

### <span data-ttu-id="30339-130">-確認</span><span class="sxs-lookup"><span data-stu-id="30339-130">-Confirm</span></span>
<span data-ttu-id="30339-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30339-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30339-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30339-132">-WhatIf</span></span>
<span data-ttu-id="30339-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30339-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30339-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30339-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30339-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30339-135">CommonParameters</span></span>
<span data-ttu-id="30339-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30339-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30339-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30339-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30339-138">輸入</span><span class="sxs-lookup"><span data-stu-id="30339-138">INPUTS</span></span>

### <span data-ttu-id="30339-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="30339-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="30339-140">System.String</span><span class="sxs-lookup"><span data-stu-id="30339-140">System.String</span></span>

## <span data-ttu-id="30339-141">輸出</span><span class="sxs-lookup"><span data-stu-id="30339-141">OUTPUTS</span></span>

### <span data-ttu-id="30339-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="30339-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="30339-143">筆記</span><span class="sxs-lookup"><span data-stu-id="30339-143">NOTES</span></span>

## <span data-ttu-id="30339-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="30339-144">RELATED LINKS</span></span>
