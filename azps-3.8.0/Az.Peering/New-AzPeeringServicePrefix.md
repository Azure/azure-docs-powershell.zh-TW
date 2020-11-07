---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: e488baacb4e9412cb4e3e5be2b6a595629495b16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958704"
---
# <span data-ttu-id="a9fea-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a9fea-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="a9fea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9fea-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fea-103">建立新的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="a9fea-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="a9fea-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9fea-104">SYNTAX</span></span>

### <span data-ttu-id="a9fea-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a9fea-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9fea-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fea-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9fea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9fea-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9fea-108">說明</span><span class="sxs-lookup"><span data-stu-id="a9fea-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fea-109">建立與對等服務物件相關聯的對等服務前置詞。</span><span class="sxs-lookup"><span data-stu-id="a9fea-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="a9fea-110">示例</span><span class="sxs-lookup"><span data-stu-id="a9fea-110">EXAMPLES</span></span>

### <span data-ttu-id="a9fea-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a9fea-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a9fea-112">從對等服務物件建立首碼</span><span class="sxs-lookup"><span data-stu-id="a9fea-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="a9fea-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a9fea-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a9fea-114">從對等服務資源識別碼建立一個前置詞。</span><span class="sxs-lookup"><span data-stu-id="a9fea-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="a9fea-115">範例3</span><span class="sxs-lookup"><span data-stu-id="a9fea-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a9fea-116">從對等服務資源群組名稱和名稱建立一個首碼</span><span class="sxs-lookup"><span data-stu-id="a9fea-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="a9fea-117">參數</span><span class="sxs-lookup"><span data-stu-id="a9fea-117">PARAMETERS</span></span>

### <span data-ttu-id="a9fea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9fea-118">-AsJob</span></span>
<span data-ttu-id="a9fea-119">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="a9fea-119">Run in the background.</span></span>

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

### <span data-ttu-id="a9fea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fea-120">-DefaultProfile</span></span>
<span data-ttu-id="a9fea-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9fea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9fea-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9fea-122">-Name</span></span>
<span data-ttu-id="a9fea-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a9fea-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fea-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="a9fea-124">-PeeringServiceId</span></span>
<span data-ttu-id="a9fea-125">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="a9fea-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fea-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="a9fea-126">-PeeringServiceName</span></span>
<span data-ttu-id="a9fea-127">對等服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a9fea-127">The peering service name.</span></span>
<span data-ttu-id="a9fea-128">針對新的對等服務，或針對清單 Get-AzPeeringService 使用 New-AzPeeringService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9fea-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fea-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="a9fea-129">-PeeringServiceObject</span></span>
<span data-ttu-id="a9fea-130">使用 Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="a9fea-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fea-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a9fea-131">-Prefix</span></span>
<span data-ttu-id="a9fea-132">會話 IPv4 首碼</span><span class="sxs-lookup"><span data-stu-id="a9fea-132">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fea-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fea-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9fea-134">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a9fea-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fea-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a9fea-135">-Confirm</span></span>
<span data-ttu-id="a9fea-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9fea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9fea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fea-137">-WhatIf</span></span>
<span data-ttu-id="a9fea-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9fea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fea-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9fea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9fea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fea-140">CommonParameters</span></span>
<span data-ttu-id="a9fea-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9fea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fea-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9fea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fea-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a9fea-143">INPUTS</span></span>

### <span data-ttu-id="a9fea-144">PSPeeringService 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="a9fea-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="a9fea-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a9fea-145">OUTPUTS</span></span>

### <span data-ttu-id="a9fea-146">PSPeeringServicePrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="a9fea-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="a9fea-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a9fea-147">NOTES</span></span>

## <span data-ttu-id="a9fea-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9fea-148">RELATED LINKS</span></span>
