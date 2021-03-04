---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: c878f7559d6e4dcfab79ae9daccaa2f82f548a62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911426"
---
# <span data-ttu-id="afdef-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="afdef-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="afdef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="afdef-102">SYNOPSIS</span></span>
<span data-ttu-id="afdef-103">從父對等資源刪除或移除已登錄的 ASN。</span><span class="sxs-lookup"><span data-stu-id="afdef-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="afdef-104">語法</span><span class="sxs-lookup"><span data-stu-id="afdef-104">SYNTAX</span></span>

### <span data-ttu-id="afdef-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="afdef-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afdef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="afdef-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afdef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="afdef-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afdef-108">描述</span><span class="sxs-lookup"><span data-stu-id="afdef-108">DESCRIPTION</span></span>
<span data-ttu-id="afdef-109">允許從父對等資源移除已登錄的 ASN。</span><span class="sxs-lookup"><span data-stu-id="afdef-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="afdef-110">例子</span><span class="sxs-lookup"><span data-stu-id="afdef-110">EXAMPLES</span></span>

### <span data-ttu-id="afdef-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="afdef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="afdef-112">根據資源識別碼移除登錄的 ASN。</span><span class="sxs-lookup"><span data-stu-id="afdef-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="afdef-113">參數</span><span class="sxs-lookup"><span data-stu-id="afdef-113">PARAMETERS</span></span>

### <span data-ttu-id="afdef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afdef-114">-AsJob</span></span>
<span data-ttu-id="afdef-115">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="afdef-115">Run in the background.</span></span>

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

### <span data-ttu-id="afdef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdef-116">-DefaultProfile</span></span>
<span data-ttu-id="afdef-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="afdef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afdef-118">-強制</span><span class="sxs-lookup"><span data-stu-id="afdef-118">-Force</span></span>
<span data-ttu-id="afdef-119">強制完成作業</span><span class="sxs-lookup"><span data-stu-id="afdef-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="afdef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afdef-120">-InputObject</span></span>
<span data-ttu-id="afdef-121">使用Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="afdef-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afdef-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="afdef-122">-Name</span></span>
<span data-ttu-id="afdef-123">登錄的 ASN 名稱</span><span class="sxs-lookup"><span data-stu-id="afdef-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afdef-124">-PassThru</span></span>
<span data-ttu-id="afdef-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="afdef-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="afdef-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="afdef-126">-PeeringName</span></span>
<span data-ttu-id="afdef-127">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="afdef-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afdef-128">-ResourceGroupName</span></span>
<span data-ttu-id="afdef-129">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="afdef-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdef-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afdef-130">-ResourceId</span></span>
<span data-ttu-id="afdef-131">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="afdef-131">The resource id string name.</span></span>

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

### <span data-ttu-id="afdef-132">-確認</span><span class="sxs-lookup"><span data-stu-id="afdef-132">-Confirm</span></span>
<span data-ttu-id="afdef-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="afdef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afdef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afdef-134">-WhatIf</span></span>
<span data-ttu-id="afdef-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afdef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afdef-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afdef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afdef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdef-137">CommonParameters</span></span>
<span data-ttu-id="afdef-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="afdef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdef-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afdef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdef-140">輸入</span><span class="sxs-lookup"><span data-stu-id="afdef-140">INPUTS</span></span>

### <span data-ttu-id="afdef-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="afdef-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="afdef-142">System.String</span><span class="sxs-lookup"><span data-stu-id="afdef-142">System.String</span></span>

## <span data-ttu-id="afdef-143">輸出</span><span class="sxs-lookup"><span data-stu-id="afdef-143">OUTPUTS</span></span>

### <span data-ttu-id="afdef-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afdef-144">System.Boolean</span></span>

## <span data-ttu-id="afdef-145">筆記</span><span class="sxs-lookup"><span data-stu-id="afdef-145">NOTES</span></span>

## <span data-ttu-id="afdef-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="afdef-146">RELATED LINKS</span></span>
