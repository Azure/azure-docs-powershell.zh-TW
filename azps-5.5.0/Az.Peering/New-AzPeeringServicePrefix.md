---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142007"
---
# <span data-ttu-id="b23ab-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b23ab-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="b23ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b23ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b23ab-103">建立新的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="b23ab-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="b23ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="b23ab-104">SYNTAX</span></span>

### <span data-ttu-id="b23ab-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b23ab-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b23ab-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b23ab-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b23ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b23ab-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b23ab-108">說明</span><span class="sxs-lookup"><span data-stu-id="b23ab-108">DESCRIPTION</span></span>
<span data-ttu-id="b23ab-109">建立與對等服務物件相關聯的對等服務前置詞。</span><span class="sxs-lookup"><span data-stu-id="b23ab-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="b23ab-110">示例</span><span class="sxs-lookup"><span data-stu-id="b23ab-110">EXAMPLES</span></span>

### <span data-ttu-id="b23ab-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b23ab-111">Example 1</span></span>
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

<span data-ttu-id="b23ab-112">從對等服務物件建立首碼</span><span class="sxs-lookup"><span data-stu-id="b23ab-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="b23ab-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b23ab-113">Example 2</span></span>
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

<span data-ttu-id="b23ab-114">從對等服務資源識別碼建立一個前置詞。</span><span class="sxs-lookup"><span data-stu-id="b23ab-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="b23ab-115">範例3</span><span class="sxs-lookup"><span data-stu-id="b23ab-115">Example 3</span></span>
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

<span data-ttu-id="b23ab-116">從對等服務資源群組名稱和名稱建立一個首碼</span><span class="sxs-lookup"><span data-stu-id="b23ab-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="b23ab-117">參數</span><span class="sxs-lookup"><span data-stu-id="b23ab-117">PARAMETERS</span></span>

### <span data-ttu-id="b23ab-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b23ab-118">-AsJob</span></span>
<span data-ttu-id="b23ab-119">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="b23ab-119">Run in the background.</span></span>

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

### <span data-ttu-id="b23ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23ab-120">-DefaultProfile</span></span>
<span data-ttu-id="b23ab-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b23ab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b23ab-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b23ab-122">-Name</span></span>
<span data-ttu-id="b23ab-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b23ab-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b23ab-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="b23ab-124">-PeeringServiceId</span></span>
<span data-ttu-id="b23ab-125">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="b23ab-125">The resource id string name.</span></span>

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

### <span data-ttu-id="b23ab-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="b23ab-126">-PeeringServiceName</span></span>
<span data-ttu-id="b23ab-127">對等服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b23ab-127">The peering service name.</span></span>
<span data-ttu-id="b23ab-128">針對新的對等服務，或針對清單 Get-AzPeeringService 使用 New-AzPeeringService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b23ab-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="b23ab-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="b23ab-129">-PeeringServiceObject</span></span>
<span data-ttu-id="b23ab-130">使用 Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="b23ab-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="b23ab-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b23ab-131">-Prefix</span></span>
<span data-ttu-id="b23ab-132">會話 IPv4 首碼</span><span class="sxs-lookup"><span data-stu-id="b23ab-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="b23ab-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b23ab-133">-ResourceGroupName</span></span>
<span data-ttu-id="b23ab-134">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b23ab-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b23ab-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="b23ab-135">-ServiceKey</span></span>
<span data-ttu-id="b23ab-136">這是您的服務提供者所提供的唯一 GUID</span><span class="sxs-lookup"><span data-stu-id="b23ab-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="b23ab-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b23ab-137">-Confirm</span></span>
<span data-ttu-id="b23ab-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b23ab-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b23ab-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b23ab-139">-WhatIf</span></span>
<span data-ttu-id="b23ab-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b23ab-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b23ab-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b23ab-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b23ab-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23ab-142">CommonParameters</span></span>
<span data-ttu-id="b23ab-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b23ab-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23ab-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b23ab-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23ab-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b23ab-145">INPUTS</span></span>

### <span data-ttu-id="b23ab-146">PSPeeringService 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b23ab-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="b23ab-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b23ab-147">OUTPUTS</span></span>

### <span data-ttu-id="b23ab-148">PSPeeringServicePrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b23ab-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="b23ab-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b23ab-149">NOTES</span></span>

## <span data-ttu-id="b23ab-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b23ab-150">RELATED LINKS</span></span>
