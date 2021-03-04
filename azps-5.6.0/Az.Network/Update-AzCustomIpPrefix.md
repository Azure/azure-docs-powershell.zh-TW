---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 9d0bca8be88c0448916df27544ce35bf7a6ddee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901849"
---
# <span data-ttu-id="1e352-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="1e352-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1e352-102">SYNOPSIS</span></span>
<span data-ttu-id="1e352-103">更新 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="1e352-104">語法</span><span class="sxs-lookup"><span data-stu-id="1e352-104">SYNTAX</span></span>

### <span data-ttu-id="1e352-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e352-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e352-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e352-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e352-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e352-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e352-108">描述</span><span class="sxs-lookup"><span data-stu-id="1e352-108">DESCRIPTION</span></span>
<span data-ttu-id="1e352-109">**Update-AzCustomIpPrefix** Cmdlet 可讓使用者傭金或解除授權其 CustomIpPrefix，或編輯資源的標籤。</span><span class="sxs-lookup"><span data-stu-id="1e352-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="1e352-110">例子</span><span class="sxs-lookup"><span data-stu-id="1e352-110">EXAMPLES</span></span>

### <span data-ttu-id="1e352-111">範例 1：傭金 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="1e352-112">上述命令會啟動 CustomIpPrefix 的啟動程式。</span><span class="sxs-lookup"><span data-stu-id="1e352-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="1e352-113">範例 2：解除授權 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="1e352-114">上述命令會啟動 CustomIpPrefix 的取消傭金程式。</span><span class="sxs-lookup"><span data-stu-id="1e352-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="1e352-115">範例 3：CustomIpPrefix 的更新標記</span><span class="sxs-lookup"><span data-stu-id="1e352-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="1e352-116">上述命令會更新 CustomIpPrefix 的標記。</span><span class="sxs-lookup"><span data-stu-id="1e352-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="1e352-117">參數</span><span class="sxs-lookup"><span data-stu-id="1e352-117">PARAMETERS</span></span>

### <span data-ttu-id="1e352-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e352-118">-AsJob</span></span>
<span data-ttu-id="1e352-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e352-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e352-120">-傭金</span><span class="sxs-lookup"><span data-stu-id="1e352-120">-Commission</span></span>
<span data-ttu-id="1e352-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e352-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e352-122">-Missionmission</span><span class="sxs-lookup"><span data-stu-id="1e352-122">-Decomission</span></span>
<span data-ttu-id="1e352-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e352-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e352-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e352-124">-DefaultProfile</span></span>
<span data-ttu-id="1e352-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e352-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e352-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e352-126">-InputObject</span></span>
<span data-ttu-id="1e352-127">要設定自訂的Prefix。</span><span class="sxs-lookup"><span data-stu-id="1e352-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e352-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e352-128">-Name</span></span>
<span data-ttu-id="1e352-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1e352-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e352-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e352-130">-ResourceGroupName</span></span>
<span data-ttu-id="1e352-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1e352-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e352-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e352-132">-ResourceId</span></span>
<span data-ttu-id="1e352-133">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e352-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e352-134">-標記</span><span class="sxs-lookup"><span data-stu-id="1e352-134">-Tag</span></span>
<span data-ttu-id="1e352-135">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1e352-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e352-136">-確認</span><span class="sxs-lookup"><span data-stu-id="1e352-136">-Confirm</span></span>
<span data-ttu-id="1e352-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1e352-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e352-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e352-138">-WhatIf</span></span>
<span data-ttu-id="1e352-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e352-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e352-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e352-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e352-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e352-141">CommonParameters</span></span>
<span data-ttu-id="1e352-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1e352-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e352-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e352-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e352-144">輸入</span><span class="sxs-lookup"><span data-stu-id="1e352-144">INPUTS</span></span>

### <span data-ttu-id="1e352-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1e352-145">System.String</span></span>

### <span data-ttu-id="1e352-146">Microsoft.Azure.Commands.Network.models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="1e352-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e352-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e352-148">輸出</span><span class="sxs-lookup"><span data-stu-id="1e352-148">OUTPUTS</span></span>

### <span data-ttu-id="1e352-149">Microsoft.Azure.Commands.Network.models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="1e352-150">筆記</span><span class="sxs-lookup"><span data-stu-id="1e352-150">NOTES</span></span>

## <span data-ttu-id="1e352-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e352-151">RELATED LINKS</span></span>

[<span data-ttu-id="1e352-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="1e352-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="1e352-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1e352-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)