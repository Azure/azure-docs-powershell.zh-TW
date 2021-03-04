---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911478"
---
# <span data-ttu-id="b6cba-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="b6cba-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="b6cba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6cba-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cba-103">取得單一物件的對等服務物件清單。</span><span class="sxs-lookup"><span data-stu-id="b6cba-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="b6cba-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6cba-104">SYNTAX</span></span>

### <span data-ttu-id="b6cba-105">ByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="b6cba-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cba-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="b6cba-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cba-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6cba-108">描述</span><span class="sxs-lookup"><span data-stu-id="b6cba-108">DESCRIPTION</span></span>
<span data-ttu-id="b6cba-109">獲得訂閱的對等服務</span><span class="sxs-lookup"><span data-stu-id="b6cba-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="b6cba-110">例子</span><span class="sxs-lookup"><span data-stu-id="b6cba-110">EXAMPLES</span></span>

### <span data-ttu-id="b6cba-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b6cba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="b6cba-112">為資源群組獲得對等服務</span><span class="sxs-lookup"><span data-stu-id="b6cba-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="b6cba-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b6cba-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="b6cba-114">為資源群組和名稱獲得對等服務</span><span class="sxs-lookup"><span data-stu-id="b6cba-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="b6cba-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="b6cba-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="b6cba-116">根據資源識別碼獲得對等服務</span><span class="sxs-lookup"><span data-stu-id="b6cba-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="b6cba-117">參數</span><span class="sxs-lookup"><span data-stu-id="b6cba-117">PARAMETERS</span></span>

### <span data-ttu-id="b6cba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cba-118">-DefaultProfile</span></span>
<span data-ttu-id="b6cba-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6cba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6cba-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6cba-120">-Name</span></span>
<span data-ttu-id="b6cba-121">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b6cba-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cba-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6cba-123">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b6cba-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="b6cba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cba-124">-ResourceId</span></span>
<span data-ttu-id="b6cba-125">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="b6cba-125">The resource id string name.</span></span>

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

### <span data-ttu-id="b6cba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cba-126">CommonParameters</span></span>
<span data-ttu-id="b6cba-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6cba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cba-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6cba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cba-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b6cba-129">INPUTS</span></span>

### <span data-ttu-id="b6cba-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b6cba-130">System.String</span></span>

## <span data-ttu-id="b6cba-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b6cba-131">OUTPUTS</span></span>

### <span data-ttu-id="b6cba-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="b6cba-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="b6cba-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b6cba-133">NOTES</span></span>

## <span data-ttu-id="b6cba-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6cba-134">RELATED LINKS</span></span>
