---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 212daeffe2ded2dd2571d78afe79fd238349bf3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911437"
---
# <span data-ttu-id="9b3d6-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="9b3d6-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="9b3d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3d6-103">建立對等物件的登錄首碼。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="9b3d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b3d6-104">SYNTAX</span></span>

### <span data-ttu-id="9b3d6-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="9b3d6-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3d6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9b3d6-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3d6-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3d6-108">描述</span><span class="sxs-lookup"><span data-stu-id="9b3d6-108">DESCRIPTION</span></span>
<span data-ttu-id="9b3d6-109">建立對等物件的登錄首碼。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="9b3d6-110">例子</span><span class="sxs-lookup"><span data-stu-id="9b3d6-110">EXAMPLES</span></span>

### <span data-ttu-id="9b3d6-111">取得對等，並建立登錄的首碼</span><span class="sxs-lookup"><span data-stu-id="9b3d6-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="9b3d6-112">取得您想要新增登錄首碼的對等。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="9b3d6-113">然後將它傳遞到 Commandlet。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="9b3d6-114">使用對等資源Id 建立登錄的 asn</span><span class="sxs-lookup"><span data-stu-id="9b3d6-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="9b3d6-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b3d6-115">PARAMETERS</span></span>

### <span data-ttu-id="9b3d6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b3d6-116">-AsJob</span></span>
<span data-ttu-id="9b3d6-117">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-117">Run in the background.</span></span>

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

### <span data-ttu-id="9b3d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3d6-118">-DefaultProfile</span></span>
<span data-ttu-id="9b3d6-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b3d6-120">-InputObject</span></span>
<span data-ttu-id="9b3d6-121">使用Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="9b3d6-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="9b3d6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b3d6-122">-Name</span></span>
<span data-ttu-id="9b3d6-123">首碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-123">The name of prefix.</span></span>

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

### <span data-ttu-id="9b3d6-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="9b3d6-124">-PeeringName</span></span>
<span data-ttu-id="9b3d6-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9b3d6-126">-首碼</span><span class="sxs-lookup"><span data-stu-id="9b3d6-126">-Prefix</span></span>
<span data-ttu-id="9b3d6-127">會話 IPv4 首碼</span><span class="sxs-lookup"><span data-stu-id="9b3d6-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="9b3d6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3d6-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b3d6-129">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="9b3d6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3d6-130">-ResourceId</span></span>
<span data-ttu-id="9b3d6-131">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-131">The resource id string name.</span></span>

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

### <span data-ttu-id="9b3d6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9b3d6-132">-Confirm</span></span>
<span data-ttu-id="9b3d6-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3d6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3d6-134">-WhatIf</span></span>
<span data-ttu-id="9b3d6-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3d6-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3d6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3d6-137">CommonParameters</span></span>
<span data-ttu-id="9b3d6-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b3d6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3d6-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b3d6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3d6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9b3d6-140">INPUTS</span></span>

### <span data-ttu-id="9b3d6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9b3d6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="9b3d6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3d6-142">System.String</span></span>

## <span data-ttu-id="9b3d6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9b3d6-143">OUTPUTS</span></span>

### <span data-ttu-id="9b3d6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="9b3d6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="9b3d6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9b3d6-145">NOTES</span></span>

## <span data-ttu-id="9b3d6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b3d6-146">RELATED LINKS</span></span>
