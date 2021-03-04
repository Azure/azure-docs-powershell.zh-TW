---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: db62779ab2ac03e6ef528b09dda99fb5ebb244a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911425"
---
# <span data-ttu-id="ac0b9-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="ac0b9-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="ac0b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ac0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0b9-103">刪除或移除父對等資源的登錄首碼。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="ac0b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="ac0b9-104">SYNTAX</span></span>

### <span data-ttu-id="ac0b9-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="ac0b9-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac0b9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac0b9-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac0b9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0b9-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac0b9-108">描述</span><span class="sxs-lookup"><span data-stu-id="ac0b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ac0b9-109">允許從父對等資源移除已登錄的首碼。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="ac0b9-110">例子</span><span class="sxs-lookup"><span data-stu-id="ac0b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ac0b9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ac0b9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="ac0b9-112">根據資源識別碼移除登錄的首碼。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="ac0b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="ac0b9-113">PARAMETERS</span></span>

### <span data-ttu-id="ac0b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac0b9-114">-AsJob</span></span>
<span data-ttu-id="ac0b9-115">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-115">Run in the background.</span></span>

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

### <span data-ttu-id="ac0b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0b9-116">-DefaultProfile</span></span>
<span data-ttu-id="ac0b9-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac0b9-118">-強制</span><span class="sxs-lookup"><span data-stu-id="ac0b9-118">-Force</span></span>
<span data-ttu-id="ac0b9-119">強制完成作業</span><span class="sxs-lookup"><span data-stu-id="ac0b9-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="ac0b9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac0b9-120">-InputObject</span></span>
<span data-ttu-id="ac0b9-121">使用Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="ac0b9-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="ac0b9-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac0b9-122">-Name</span></span>
<span data-ttu-id="ac0b9-123">首碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-123">The name of prefix.</span></span>

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

### <span data-ttu-id="ac0b9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac0b9-124">-PassThru</span></span>
<span data-ttu-id="ac0b9-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ac0b9-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ac0b9-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="ac0b9-126">-PeeringName</span></span>
<span data-ttu-id="ac0b9-127">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ac0b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac0b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="ac0b9-129">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ac0b9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0b9-130">-ResourceId</span></span>
<span data-ttu-id="ac0b9-131">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-131">The resource id string name.</span></span>

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

### <span data-ttu-id="ac0b9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ac0b9-132">-Confirm</span></span>
<span data-ttu-id="ac0b9-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac0b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac0b9-134">-WhatIf</span></span>
<span data-ttu-id="ac0b9-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac0b9-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac0b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0b9-137">CommonParameters</span></span>
<span data-ttu-id="ac0b9-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ac0b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0b9-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac0b9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0b9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ac0b9-140">INPUTS</span></span>

### <span data-ttu-id="ac0b9-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ac0b9-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="ac0b9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ac0b9-142">System.String</span></span>

## <span data-ttu-id="ac0b9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ac0b9-143">OUTPUTS</span></span>

### <span data-ttu-id="ac0b9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac0b9-144">System.Boolean</span></span>

## <span data-ttu-id="ac0b9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ac0b9-145">NOTES</span></span>

## <span data-ttu-id="ac0b9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac0b9-146">RELATED LINKS</span></span>
