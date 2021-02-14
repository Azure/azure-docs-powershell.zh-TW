---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134743"
---
# <span data-ttu-id="b6650-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b6650-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b6650-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6650-102">SYNOPSIS</span></span>
<span data-ttu-id="b6650-103">取得或列出 peerings 的已註冊前置詞。</span><span class="sxs-lookup"><span data-stu-id="b6650-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="b6650-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6650-104">SYNTAX</span></span>

### <span data-ttu-id="b6650-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="b6650-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6650-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6650-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6650-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6650-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6650-108">說明</span><span class="sxs-lookup"><span data-stu-id="b6650-108">DESCRIPTION</span></span>
<span data-ttu-id="b6650-109">取得或列出 peerings 的已註冊前置詞。</span><span class="sxs-lookup"><span data-stu-id="b6650-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="b6650-110">示例</span><span class="sxs-lookup"><span data-stu-id="b6650-110">EXAMPLES</span></span>

### <span data-ttu-id="b6650-111">列出對等的已註冊 ASNs</span><span class="sxs-lookup"><span data-stu-id="b6650-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="b6650-112">列出已註冊的 asn。</span><span class="sxs-lookup"><span data-stu-id="b6650-112">Lists registered asn.</span></span>

### <span data-ttu-id="b6650-113">透過名稱取得對等的註冊 ASN</span><span class="sxs-lookup"><span data-stu-id="b6650-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="b6650-114">取得已註冊的對等 asn。</span><span class="sxs-lookup"><span data-stu-id="b6650-114">Gets registered peering asn.</span></span>

<span data-ttu-id="b6650-115">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="b6650-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="b6650-116">參數</span><span class="sxs-lookup"><span data-stu-id="b6650-116">PARAMETERS</span></span>

### <span data-ttu-id="b6650-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6650-117">-DefaultProfile</span></span>
<span data-ttu-id="b6650-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6650-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6650-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6650-119">-InputObject</span></span>
<span data-ttu-id="b6650-120">使用 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b6650-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="b6650-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6650-121">-Name</span></span>
<span data-ttu-id="b6650-122">前置詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6650-122">The name of prefix.</span></span>

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

### <span data-ttu-id="b6650-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b6650-123">-PeeringName</span></span>
<span data-ttu-id="b6650-124">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b6650-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b6650-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6650-125">-ResourceGroupName</span></span>
<span data-ttu-id="b6650-126">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b6650-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b6650-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6650-127">-ResourceId</span></span>
<span data-ttu-id="b6650-128">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="b6650-128">The resource id string name.</span></span>

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

### <span data-ttu-id="b6650-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6650-129">CommonParameters</span></span>
<span data-ttu-id="b6650-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6650-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6650-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6650-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6650-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b6650-132">INPUTS</span></span>

### <span data-ttu-id="b6650-133">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b6650-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b6650-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b6650-134">System.String</span></span>

## <span data-ttu-id="b6650-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b6650-135">OUTPUTS</span></span>

### <span data-ttu-id="b6650-136">PSPeeringRegisteredPrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b6650-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b6650-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b6650-137">NOTES</span></span>

## <span data-ttu-id="b6650-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6650-138">RELATED LINKS</span></span>
