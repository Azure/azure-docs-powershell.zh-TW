---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: d36561e2090e5b98bed5a5051715fe3e868bde4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965926"
---
# <span data-ttu-id="78901-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="78901-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="78901-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78901-102">SYNOPSIS</span></span>
<span data-ttu-id="78901-103">取得訂閱的對等服務首碼清單。</span><span class="sxs-lookup"><span data-stu-id="78901-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="78901-104">句法</span><span class="sxs-lookup"><span data-stu-id="78901-104">SYNTAX</span></span>

### <span data-ttu-id="78901-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="78901-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78901-106">設置</span><span class="sxs-lookup"><span data-stu-id="78901-106">Default</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78901-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78901-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78901-108">說明</span><span class="sxs-lookup"><span data-stu-id="78901-108">DESCRIPTION</span></span>
<span data-ttu-id="78901-109">列出對等服務物件的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="78901-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="78901-110">示例</span><span class="sxs-lookup"><span data-stu-id="78901-110">EXAMPLES</span></span>

### <span data-ttu-id="78901-111">範例1</span><span class="sxs-lookup"><span data-stu-id="78901-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="78901-112">根據管道命令取得對等服務的首碼。</span><span class="sxs-lookup"><span data-stu-id="78901-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="78901-113">範例2</span><span class="sxs-lookup"><span data-stu-id="78901-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="78901-114">針對資源識別碼，取得對等服務的特定前置詞。</span><span class="sxs-lookup"><span data-stu-id="78901-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="78901-115">範例3</span><span class="sxs-lookup"><span data-stu-id="78901-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="78901-116">針對資源識別碼，取得對等服務的特定前置詞。</span><span class="sxs-lookup"><span data-stu-id="78901-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="78901-117">範例4</span><span class="sxs-lookup"><span data-stu-id="78901-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="78901-118">針對具有展開屬性的對等服務取得特定的前置詞</span><span class="sxs-lookup"><span data-stu-id="78901-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="78901-119">參數</span><span class="sxs-lookup"><span data-stu-id="78901-119">PARAMETERS</span></span>

### <span data-ttu-id="78901-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78901-120">-DefaultProfile</span></span>
<span data-ttu-id="78901-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78901-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78901-122">-展開</span><span class="sxs-lookup"><span data-stu-id="78901-122">-Expand</span></span>
<span data-ttu-id="78901-123">查看對等服務首碼的事件</span><span class="sxs-lookup"><span data-stu-id="78901-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="78901-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="78901-124">-Name</span></span>
<span data-ttu-id="78901-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="78901-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78901-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="78901-126">-PeeringServiceName</span></span>
<span data-ttu-id="78901-127">對等服務名稱。</span><span class="sxs-lookup"><span data-stu-id="78901-127">The peering service name.</span></span> <span data-ttu-id="78901-128">針對新的對等服務，或針對清單 Get-AzPeeringService 使用 New-AzPeeringService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78901-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="78901-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="78901-129">-PeeringServiceObject</span></span>
<span data-ttu-id="78901-130">使用 Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="78901-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78901-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78901-131">-ResourceGroupName</span></span>
<span data-ttu-id="78901-132">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="78901-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="78901-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78901-133">-ResourceId</span></span>
<span data-ttu-id="78901-134">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="78901-134">The resource id string name.</span></span>

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

### <span data-ttu-id="78901-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78901-135">CommonParameters</span></span>
<span data-ttu-id="78901-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78901-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78901-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78901-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78901-138">輸入</span><span class="sxs-lookup"><span data-stu-id="78901-138">INPUTS</span></span>

### <span data-ttu-id="78901-139">PSPeeringService 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="78901-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="78901-140">System.object</span><span class="sxs-lookup"><span data-stu-id="78901-140">System.String</span></span>

## <span data-ttu-id="78901-141">輸出</span><span class="sxs-lookup"><span data-stu-id="78901-141">OUTPUTS</span></span>

### <span data-ttu-id="78901-142">PSPeeringServicePrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="78901-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="78901-143">筆記</span><span class="sxs-lookup"><span data-stu-id="78901-143">NOTES</span></span>

## <span data-ttu-id="78901-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="78901-144">RELATED LINKS</span></span>
