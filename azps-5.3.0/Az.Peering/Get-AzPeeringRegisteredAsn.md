---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437420"
---
# <span data-ttu-id="b47ef-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b47ef-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b47ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b47ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b47ef-103">取得網際網路交換路由伺服器類型 peerings 的註冊 ASN。</span><span class="sxs-lookup"><span data-stu-id="b47ef-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="b47ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="b47ef-104">SYNTAX</span></span>

### <span data-ttu-id="b47ef-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="b47ef-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b47ef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b47ef-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b47ef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b47ef-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b47ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="b47ef-108">DESCRIPTION</span></span>
<span data-ttu-id="b47ef-109">取得或列出已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="b47ef-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="b47ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="b47ef-110">EXAMPLES</span></span>

### <span data-ttu-id="b47ef-111">列出對等的已註冊 ASNs</span><span class="sxs-lookup"><span data-stu-id="b47ef-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="b47ef-112">列出已註冊的 asn。</span><span class="sxs-lookup"><span data-stu-id="b47ef-112">Lists registered asn.</span></span>

### <span data-ttu-id="b47ef-113">透過名稱取得對等的註冊 ASN</span><span class="sxs-lookup"><span data-stu-id="b47ef-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="b47ef-114">取得已註冊的對等 asn。</span><span class="sxs-lookup"><span data-stu-id="b47ef-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="b47ef-115">參數</span><span class="sxs-lookup"><span data-stu-id="b47ef-115">PARAMETERS</span></span>

### <span data-ttu-id="b47ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47ef-116">-DefaultProfile</span></span>
<span data-ttu-id="b47ef-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b47ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b47ef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b47ef-118">-InputObject</span></span>
<span data-ttu-id="b47ef-119">使用 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b47ef-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="b47ef-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b47ef-120">-Name</span></span>
<span data-ttu-id="b47ef-121">已註冊 ASN 的名稱</span><span class="sxs-lookup"><span data-stu-id="b47ef-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="b47ef-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b47ef-122">-PeeringName</span></span>
<span data-ttu-id="b47ef-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b47ef-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b47ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="b47ef-125">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b47ef-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b47ef-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b47ef-126">-ResourceId</span></span>
<span data-ttu-id="b47ef-127">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="b47ef-127">The resource id string name.</span></span>

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

### <span data-ttu-id="b47ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47ef-128">CommonParameters</span></span>
<span data-ttu-id="b47ef-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b47ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47ef-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b47ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47ef-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b47ef-131">INPUTS</span></span>

### <span data-ttu-id="b47ef-132">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b47ef-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b47ef-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b47ef-133">System.String</span></span>

## <span data-ttu-id="b47ef-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b47ef-134">OUTPUTS</span></span>

### <span data-ttu-id="b47ef-135">PSPeeringRegisteredAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b47ef-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b47ef-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b47ef-136">NOTES</span></span>

## <span data-ttu-id="b47ef-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b47ef-137">RELATED LINKS</span></span>
