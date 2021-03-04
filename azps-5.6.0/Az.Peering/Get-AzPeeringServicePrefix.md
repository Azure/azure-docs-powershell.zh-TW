---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 8b62189848583d11738a39555bc80ed0a52776fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911473"
---
# <span data-ttu-id="6a5bf-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="6a5bf-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="6a5bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5bf-103">獲得訂閱的對等服務首碼清單。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="6a5bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a5bf-104">SYNTAX</span></span>

### <span data-ttu-id="6a5bf-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="6a5bf-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a5bf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a5bf-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a5bf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a5bf-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a5bf-108">描述</span><span class="sxs-lookup"><span data-stu-id="6a5bf-108">DESCRIPTION</span></span>
<span data-ttu-id="6a5bf-109">對等服務物件的清單對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="6a5bf-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="6a5bf-110">例子</span><span class="sxs-lookup"><span data-stu-id="6a5bf-110">EXAMPLES</span></span>

### <span data-ttu-id="6a5bf-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6a5bf-111">Example 1</span></span>
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

<span data-ttu-id="6a5bf-112">根據管線命令，獲得對等服務的首碼。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="6a5bf-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="6a5bf-113">Example 2</span></span>
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

<span data-ttu-id="6a5bf-114">根據資源識別碼，為對等服務獲得特定的首碼。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="6a5bf-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="6a5bf-115">Example 3</span></span>
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

<span data-ttu-id="6a5bf-116">根據資源識別碼，為對等服務獲得特定的首碼。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="6a5bf-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="6a5bf-117">Example 4</span></span>
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

<span data-ttu-id="6a5bf-118">使用展開的屬性為對等服務獲得特定的首碼</span><span class="sxs-lookup"><span data-stu-id="6a5bf-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="6a5bf-119">參數</span><span class="sxs-lookup"><span data-stu-id="6a5bf-119">PARAMETERS</span></span>

### <span data-ttu-id="6a5bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5bf-120">-DefaultProfile</span></span>
<span data-ttu-id="6a5bf-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5bf-122">-展開</span><span class="sxs-lookup"><span data-stu-id="6a5bf-122">-Expand</span></span>
<span data-ttu-id="6a5bf-123">查看對等服務首碼的事件</span><span class="sxs-lookup"><span data-stu-id="6a5bf-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="6a5bf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a5bf-124">-Name</span></span>
<span data-ttu-id="6a5bf-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5bf-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="6a5bf-126">-PeeringServiceName</span></span>
<span data-ttu-id="6a5bf-127">對等服務名稱。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-127">The peering service name.</span></span> <span data-ttu-id="6a5bf-128">使用 New-AzPeeringService Cmdlet 來建立新的對等Get-AzPeeringService清單。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="6a5bf-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="6a5bf-129">-PeeringServiceObject</span></span>
<span data-ttu-id="6a5bf-130">使用Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="6a5bf-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5bf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5bf-131">-ResourceGroupName</span></span>
<span data-ttu-id="6a5bf-132">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="6a5bf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a5bf-133">-ResourceId</span></span>
<span data-ttu-id="6a5bf-134">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-134">The resource id string name.</span></span>

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

### <span data-ttu-id="6a5bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5bf-135">CommonParameters</span></span>
<span data-ttu-id="6a5bf-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a5bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5bf-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a5bf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5bf-138">輸入</span><span class="sxs-lookup"><span data-stu-id="6a5bf-138">INPUTS</span></span>

### <span data-ttu-id="6a5bf-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="6a5bf-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="6a5bf-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6a5bf-140">System.String</span></span>

## <span data-ttu-id="6a5bf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="6a5bf-141">OUTPUTS</span></span>

### <span data-ttu-id="6a5bf-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="6a5bf-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="6a5bf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6a5bf-143">NOTES</span></span>

## <span data-ttu-id="6a5bf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a5bf-144">RELATED LINKS</span></span>
