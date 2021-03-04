---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 4218dd5441c4f580c89d770556f2d5c329cfd06c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911502"
---
# <span data-ttu-id="6b660-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6b660-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6b660-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6b660-102">SYNOPSIS</span></span>
<span data-ttu-id="6b660-103">針對網際網路交換路由伺服器類型對等，獲得登錄的 ASN。</span><span class="sxs-lookup"><span data-stu-id="6b660-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="6b660-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b660-104">SYNTAX</span></span>

### <span data-ttu-id="6b660-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="6b660-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b660-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6b660-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b660-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b660-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b660-108">描述</span><span class="sxs-lookup"><span data-stu-id="6b660-108">DESCRIPTION</span></span>
<span data-ttu-id="6b660-109">取得或列出已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="6b660-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="6b660-110">例子</span><span class="sxs-lookup"><span data-stu-id="6b660-110">EXAMPLES</span></span>

### <span data-ttu-id="6b660-111">清單已註冊的 ASN 以對等</span><span class="sxs-lookup"><span data-stu-id="6b660-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="6b660-112">已註冊 asn 的清單。</span><span class="sxs-lookup"><span data-stu-id="6b660-112">Lists registered asn.</span></span>

### <span data-ttu-id="6b660-113">以名稱註冊 ASN 進行對等</span><span class="sxs-lookup"><span data-stu-id="6b660-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="6b660-114">獲得註冊的對等對等 asn。</span><span class="sxs-lookup"><span data-stu-id="6b660-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="6b660-115">參數</span><span class="sxs-lookup"><span data-stu-id="6b660-115">PARAMETERS</span></span>

### <span data-ttu-id="6b660-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b660-116">-DefaultProfile</span></span>
<span data-ttu-id="6b660-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b660-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b660-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b660-118">-InputObject</span></span>
<span data-ttu-id="6b660-119">使用Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6b660-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b660-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b660-120">-Name</span></span>
<span data-ttu-id="6b660-121">登錄的 ASN 名稱</span><span class="sxs-lookup"><span data-stu-id="6b660-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="6b660-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="6b660-122">-PeeringName</span></span>
<span data-ttu-id="6b660-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="6b660-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="6b660-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b660-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b660-125">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6b660-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="6b660-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b660-126">-ResourceId</span></span>
<span data-ttu-id="6b660-127">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="6b660-127">The resource id string name.</span></span>

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

### <span data-ttu-id="6b660-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b660-128">CommonParameters</span></span>
<span data-ttu-id="6b660-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6b660-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b660-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b660-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b660-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6b660-131">INPUTS</span></span>

### <span data-ttu-id="6b660-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6b660-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="6b660-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6b660-133">System.String</span></span>

## <span data-ttu-id="6b660-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6b660-134">OUTPUTS</span></span>

### <span data-ttu-id="6b660-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6b660-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6b660-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6b660-136">NOTES</span></span>

## <span data-ttu-id="6b660-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b660-137">RELATED LINKS</span></span>
