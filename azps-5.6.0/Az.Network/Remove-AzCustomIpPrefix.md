---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: d4fcdb1ad5606753980ea323137d0b77a8580ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908086"
---
# <span data-ttu-id="c6d1d-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1d-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="c6d1d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d1d-103">移除 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1d-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="c6d1d-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6d1d-104">SYNTAX</span></span>

### <span data-ttu-id="c6d1d-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6d1d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6d1d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6d1d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6d1d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6d1d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6d1d-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6d1d-108">DESCRIPTION</span></span>
<span data-ttu-id="c6d1d-109">**Remove-AzCustomIpPrefix** Cmdlet 會移除 CustomIpPrefix。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="c6d1d-110">例子</span><span class="sxs-lookup"><span data-stu-id="c6d1d-110">EXAMPLES</span></span>

### <span data-ttu-id="c6d1d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c6d1d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="c6d1d-112">從資源群組移除具有名稱$prefixName的 CustomIpPrefix $rgName</span><span class="sxs-lookup"><span data-stu-id="c6d1d-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="c6d1d-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6d1d-113">PARAMETERS</span></span>

### <span data-ttu-id="c6d1d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6d1d-114">-AsJob</span></span>
<span data-ttu-id="c6d1d-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6d1d-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d1d-116">-DefaultProfile</span></span>
<span data-ttu-id="c6d1d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-118">-強制</span><span class="sxs-lookup"><span data-stu-id="c6d1d-118">-Force</span></span>
<span data-ttu-id="c6d1d-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6d1d-120">-InputObject</span></span>
<span data-ttu-id="c6d1d-121">customIpPrefix 物件。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6d1d-122">-Name</span></span>
<span data-ttu-id="c6d1d-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6d1d-124">-PassThru</span></span>
<span data-ttu-id="c6d1d-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c6d1d-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6d1d-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6d1d-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6d1d-129">-ResourceId</span></span>
<span data-ttu-id="c6d1d-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c6d1d-131">-Confirm</span></span>
<span data-ttu-id="c6d1d-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6d1d-133">-WhatIf</span></span>
<span data-ttu-id="c6d1d-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6d1d-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d1d-136">CommonParameters</span></span>
<span data-ttu-id="c6d1d-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6d1d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d1d-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6d1d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d1d-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c6d1d-139">INPUTS</span></span>

### <span data-ttu-id="c6d1d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c6d1d-140">System.String</span></span>

### <span data-ttu-id="c6d1d-141">Microsoft.Azure.Commands.Network.models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1d-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="c6d1d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c6d1d-142">OUTPUTS</span></span>

### <span data-ttu-id="c6d1d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6d1d-143">System.Boolean</span></span>

## <span data-ttu-id="c6d1d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c6d1d-144">NOTES</span></span>

## <span data-ttu-id="c6d1d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6d1d-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6d1d-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1d-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="c6d1d-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1d-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="c6d1d-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1d-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)