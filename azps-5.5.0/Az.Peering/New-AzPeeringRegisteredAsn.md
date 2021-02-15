---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140150"
---
# <span data-ttu-id="e348e-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="e348e-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="e348e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e348e-102">SYNOPSIS</span></span>
<span data-ttu-id="e348e-103">建立對等的註冊 ASN</span><span class="sxs-lookup"><span data-stu-id="e348e-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="e348e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e348e-104">SYNTAX</span></span>

### <span data-ttu-id="e348e-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="e348e-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e348e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e348e-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e348e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e348e-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e348e-108">說明</span><span class="sxs-lookup"><span data-stu-id="e348e-108">DESCRIPTION</span></span>
<span data-ttu-id="e348e-109">針對對等物件建立已註冊的 ASNs。</span><span class="sxs-lookup"><span data-stu-id="e348e-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="e348e-110">示例</span><span class="sxs-lookup"><span data-stu-id="e348e-110">EXAMPLES</span></span>

### <span data-ttu-id="e348e-111">取得對等與建立已註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="e348e-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="e348e-112">取得您想要新增已註冊 ASN 的對等。</span><span class="sxs-lookup"><span data-stu-id="e348e-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="e348e-113">然後將它傳遞到 commandlet。</span><span class="sxs-lookup"><span data-stu-id="e348e-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="e348e-114">使用對等 resourceId 建立已註冊的 asn</span><span class="sxs-lookup"><span data-stu-id="e348e-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="e348e-115">參數</span><span class="sxs-lookup"><span data-stu-id="e348e-115">PARAMETERS</span></span>

### <span data-ttu-id="e348e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e348e-116">-AsJob</span></span>
<span data-ttu-id="e348e-117">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="e348e-117">Run in the background.</span></span>

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

### <span data-ttu-id="e348e-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="e348e-118">-Asn</span></span>
<span data-ttu-id="e348e-119">要註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="e348e-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e348e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e348e-120">-DefaultProfile</span></span>
<span data-ttu-id="e348e-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e348e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e348e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e348e-122">-InputObject</span></span>
<span data-ttu-id="e348e-123">使用 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e348e-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e348e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e348e-124">-Name</span></span>
<span data-ttu-id="e348e-125">要註冊的 ASN</span><span class="sxs-lookup"><span data-stu-id="e348e-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e348e-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e348e-126">-PeeringName</span></span>
<span data-ttu-id="e348e-127">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="e348e-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e348e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e348e-128">-ResourceGroupName</span></span>
<span data-ttu-id="e348e-129">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e348e-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e348e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e348e-130">-ResourceId</span></span>
<span data-ttu-id="e348e-131">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="e348e-131">The resource id string name.</span></span>

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

### <span data-ttu-id="e348e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e348e-132">-Confirm</span></span>
<span data-ttu-id="e348e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e348e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e348e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e348e-134">-WhatIf</span></span>
<span data-ttu-id="e348e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e348e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e348e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e348e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e348e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e348e-137">CommonParameters</span></span>
<span data-ttu-id="e348e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e348e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e348e-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e348e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e348e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e348e-140">INPUTS</span></span>

### <span data-ttu-id="e348e-141">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="e348e-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e348e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="e348e-142">System.String</span></span>

## <span data-ttu-id="e348e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e348e-143">OUTPUTS</span></span>

### <span data-ttu-id="e348e-144">PSPeeringRegisteredAsn 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="e348e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="e348e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e348e-145">NOTES</span></span>

## <span data-ttu-id="e348e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e348e-146">RELATED LINKS</span></span>
