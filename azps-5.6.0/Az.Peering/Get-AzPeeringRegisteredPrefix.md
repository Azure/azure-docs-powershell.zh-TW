---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 4eb704682885e5040913e08c5242d4142a387ef7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911482"
---
# <span data-ttu-id="e1164-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e1164-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e1164-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1164-102">SYNOPSIS</span></span>
<span data-ttu-id="e1164-103">獲得或列出對等互連的登錄首碼。</span><span class="sxs-lookup"><span data-stu-id="e1164-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="e1164-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1164-104">SYNTAX</span></span>

### <span data-ttu-id="e1164-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="e1164-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1164-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1164-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1164-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1164-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1164-108">描述</span><span class="sxs-lookup"><span data-stu-id="e1164-108">DESCRIPTION</span></span>
<span data-ttu-id="e1164-109">獲得或列出對等互連的登錄首碼。</span><span class="sxs-lookup"><span data-stu-id="e1164-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="e1164-110">例子</span><span class="sxs-lookup"><span data-stu-id="e1164-110">EXAMPLES</span></span>

### <span data-ttu-id="e1164-111">清單已註冊的 ASN 以對等</span><span class="sxs-lookup"><span data-stu-id="e1164-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="e1164-112">已註冊 asn 的清單。</span><span class="sxs-lookup"><span data-stu-id="e1164-112">Lists registered asn.</span></span>

### <span data-ttu-id="e1164-113">以名稱註冊 ASN 進行對等</span><span class="sxs-lookup"><span data-stu-id="e1164-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="e1164-114">獲得註冊的對等對等 asn。</span><span class="sxs-lookup"><span data-stu-id="e1164-114">Gets registered peering asn.</span></span>

<span data-ttu-id="e1164-115">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="e1164-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="e1164-116">參數</span><span class="sxs-lookup"><span data-stu-id="e1164-116">PARAMETERS</span></span>

### <span data-ttu-id="e1164-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1164-117">-DefaultProfile</span></span>
<span data-ttu-id="e1164-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1164-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1164-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1164-119">-InputObject</span></span>
<span data-ttu-id="e1164-120">使用Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e1164-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="e1164-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1164-121">-Name</span></span>
<span data-ttu-id="e1164-122">首碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1164-122">The name of prefix.</span></span>

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

### <span data-ttu-id="e1164-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e1164-123">-PeeringName</span></span>
<span data-ttu-id="e1164-124">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="e1164-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e1164-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1164-125">-ResourceGroupName</span></span>
<span data-ttu-id="e1164-126">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e1164-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e1164-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1164-127">-ResourceId</span></span>
<span data-ttu-id="e1164-128">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="e1164-128">The resource id string name.</span></span>

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

### <span data-ttu-id="e1164-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1164-129">CommonParameters</span></span>
<span data-ttu-id="e1164-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1164-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1164-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1164-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1164-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e1164-132">INPUTS</span></span>

### <span data-ttu-id="e1164-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e1164-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e1164-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e1164-134">System.String</span></span>

## <span data-ttu-id="e1164-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e1164-135">OUTPUTS</span></span>

### <span data-ttu-id="e1164-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e1164-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e1164-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e1164-137">NOTES</span></span>

## <span data-ttu-id="e1164-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1164-138">RELATED LINKS</span></span>
