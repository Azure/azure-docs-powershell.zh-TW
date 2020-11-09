---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287820"
---
# <span data-ttu-id="2f9f9-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="2f9f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9f9-103">更新 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="2f9f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f9f9-104">SYNTAX</span></span>

### <span data-ttu-id="2f9f9-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f9f9-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f9f9-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f9f9-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f9f9-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f9f9-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f9f9-108">說明</span><span class="sxs-lookup"><span data-stu-id="2f9f9-108">DESCRIPTION</span></span>
<span data-ttu-id="2f9f9-109">**AzCustomIpPrefix** Cmdlet 可讓使用者在傭金或解除其 CustomIpPrefix，或編輯資源的標籤。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="2f9f9-110">示例</span><span class="sxs-lookup"><span data-stu-id="2f9f9-110">EXAMPLES</span></span>

### <span data-ttu-id="2f9f9-111">範例1：傭金為 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="2f9f9-112">上述命令會啟動 CustomIpPrefix 的 commissioning 進程。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="2f9f9-113">範例2：解除 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="2f9f9-114">上述命令會啟動 CustomIpPrefix 的取消 commissioning 進程。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="2f9f9-115">範例3：更新 CustomIpPrefix 的標記</span><span class="sxs-lookup"><span data-stu-id="2f9f9-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="2f9f9-116">上述命令會更新 CustomIpPrefix 的標記。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="2f9f9-117">參數</span><span class="sxs-lookup"><span data-stu-id="2f9f9-117">PARAMETERS</span></span>

### <span data-ttu-id="2f9f9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f9f9-118">-AsJob</span></span>
<span data-ttu-id="2f9f9-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f9f9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f9f9-120">-傭金</span><span class="sxs-lookup"><span data-stu-id="2f9f9-120">-Commission</span></span>
<span data-ttu-id="2f9f9-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f9f9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f9f9-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="2f9f9-122">-Decomission</span></span>
<span data-ttu-id="2f9f9-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f9f9-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f9f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9f9-124">-DefaultProfile</span></span>
<span data-ttu-id="2f9f9-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f9f9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f9f9-126">-InputObject</span></span>
<span data-ttu-id="2f9f9-127">要設定的 CustomIpPrefix。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="2f9f9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f9f9-128">-Name</span></span>
<span data-ttu-id="2f9f9-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-129">The resource name.</span></span>

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

### <span data-ttu-id="2f9f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f9f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="2f9f9-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-131">The resource group name.</span></span>

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

### <span data-ttu-id="2f9f9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f9f9-132">-ResourceId</span></span>
<span data-ttu-id="2f9f9-133">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-133">The resource Id.</span></span>

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

### <span data-ttu-id="2f9f9-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f9f9-134">-Tag</span></span>
<span data-ttu-id="2f9f9-135">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2f9f9-136">-確認</span><span class="sxs-lookup"><span data-stu-id="2f9f9-136">-Confirm</span></span>
<span data-ttu-id="2f9f9-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f9f9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f9f9-138">-WhatIf</span></span>
<span data-ttu-id="2f9f9-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f9f9-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f9f9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9f9-141">CommonParameters</span></span>
<span data-ttu-id="2f9f9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9f9-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2f9f9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9f9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="2f9f9-144">INPUTS</span></span>

### <span data-ttu-id="2f9f9-145">System.object</span><span class="sxs-lookup"><span data-stu-id="2f9f9-145">System.String</span></span>

### <span data-ttu-id="2f9f9-146">PSCustomIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f9f9-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="2f9f9-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f9f9-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2f9f9-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2f9f9-148">OUTPUTS</span></span>

### <span data-ttu-id="2f9f9-149">PSCustomIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f9f9-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="2f9f9-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2f9f9-150">NOTES</span></span>

## <span data-ttu-id="2f9f9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f9f9-151">RELATED LINKS</span></span>

[<span data-ttu-id="2f9f9-152">AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="2f9f9-153">新-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="2f9f9-154">移除-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2f9f9-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)