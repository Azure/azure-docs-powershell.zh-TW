---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281166"
---
# <span data-ttu-id="f54a2-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="f54a2-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="f54a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f54a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f54a2-103">取得單一物件之對等服務物件的清單。</span><span class="sxs-lookup"><span data-stu-id="f54a2-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="f54a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f54a2-104">SYNTAX</span></span>

### <span data-ttu-id="f54a2-105">ByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="f54a2-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f54a2-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="f54a2-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f54a2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f54a2-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54a2-108">說明</span><span class="sxs-lookup"><span data-stu-id="f54a2-108">DESCRIPTION</span></span>
<span data-ttu-id="f54a2-109">取得訂閱的對等服務</span><span class="sxs-lookup"><span data-stu-id="f54a2-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="f54a2-110">示例</span><span class="sxs-lookup"><span data-stu-id="f54a2-110">EXAMPLES</span></span>

### <span data-ttu-id="f54a2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f54a2-111">Example 1</span></span>
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

<span data-ttu-id="f54a2-112">取得資源群組的對等服務</span><span class="sxs-lookup"><span data-stu-id="f54a2-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="f54a2-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f54a2-113">Example 2</span></span>
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

<span data-ttu-id="f54a2-114">取得資源群組和名稱的對等服務</span><span class="sxs-lookup"><span data-stu-id="f54a2-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="f54a2-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f54a2-115">Example 3</span></span>
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

<span data-ttu-id="f54a2-116">依資源識別碼取得對等服務</span><span class="sxs-lookup"><span data-stu-id="f54a2-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="f54a2-117">參數</span><span class="sxs-lookup"><span data-stu-id="f54a2-117">PARAMETERS</span></span>

### <span data-ttu-id="f54a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54a2-118">-DefaultProfile</span></span>
<span data-ttu-id="f54a2-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f54a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f54a2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f54a2-120">-Name</span></span>
<span data-ttu-id="f54a2-121">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="f54a2-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f54a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f54a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f54a2-123">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f54a2-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f54a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f54a2-124">-ResourceId</span></span>
<span data-ttu-id="f54a2-125">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="f54a2-125">The resource id string name.</span></span>

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

### <span data-ttu-id="f54a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54a2-126">CommonParameters</span></span>
<span data-ttu-id="f54a2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f54a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54a2-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f54a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54a2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f54a2-129">INPUTS</span></span>

### <span data-ttu-id="f54a2-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f54a2-130">System.String</span></span>

## <span data-ttu-id="f54a2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f54a2-131">OUTPUTS</span></span>

### <span data-ttu-id="f54a2-132">PSPeeringService 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="f54a2-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="f54a2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f54a2-133">NOTES</span></span>

## <span data-ttu-id="f54a2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f54a2-134">RELATED LINKS</span></span>
