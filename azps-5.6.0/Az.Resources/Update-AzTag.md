---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: acf97f282e50d9c6f468e400cb2a5c598fe06659
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913661"
---
# <span data-ttu-id="c5694-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="c5694-101">Update-AzTag</span></span>

## <span data-ttu-id="c5694-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5694-102">SYNOPSIS</span></span>

<span data-ttu-id="c5694-103">選擇性地更新資源或訂閱上的一組標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="c5694-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5694-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="c5694-105">描述</span><span class="sxs-lookup"><span data-stu-id="c5694-105">DESCRIPTION</span></span>

<span data-ttu-id="c5694-106">具有 **ResourceId** **的更新-AzTag** Cmdlet 選擇性地更新資源或訂閱上的一組標籤。</span><span class="sxs-lookup"><span data-stu-id="c5694-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="c5694-107">這項作業允許取代、合併或選擇性刪除指定資源或訂閱上的標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="c5694-108">指定實體在作業結束時最多可以有 50 個標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="c5694-109">'replace' 選項會以新集合取代整組現有標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="c5694-110">使用 'merge' 選項可新增具有新名稱的標記，並更新現有名稱的標記值。</span><span class="sxs-lookup"><span data-stu-id="c5694-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="c5694-111">'delete' 選項允許根據指定名稱或名稱/值組選擇性刪除標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="c5694-112">例子</span><span class="sxs-lookup"><span data-stu-id="c5694-112">EXAMPLES</span></span>

### <span data-ttu-id="c5694-113">範例 1：選擇性地使用「合併」作業更新訂閱上的一組標記</span><span class="sxs-lookup"><span data-stu-id="c5694-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="c5694-114">此命令會將訂閱上的一組標記與 {subId} 合併。</span><span class="sxs-lookup"><span data-stu-id="c5694-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="c5694-115">範例 2：選擇性地以「取代」作業更新訂閱上的一組標記</span><span class="sxs-lookup"><span data-stu-id="c5694-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="c5694-116">此命令會使用 {subId} 重新設定訂閱上的一組標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="c5694-117">範例 3：選擇性地使用「刪除」作業更新訂閱上的一組標記</span><span class="sxs-lookup"><span data-stu-id="c5694-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="c5694-118">此命令會使用 {subId} 刪除訂閱上的一組標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="c5694-119">參數</span><span class="sxs-lookup"><span data-stu-id="c5694-119">PARAMETERS</span></span>

### <span data-ttu-id="c5694-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5694-120">-DefaultProfile</span></span>
<span data-ttu-id="c5694-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5694-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5694-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5694-122">-ResourceId</span></span>
<span data-ttu-id="c5694-123">標記實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5694-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="c5694-124">系統可能會標記資源、資源群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5694-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5694-125">-標記</span><span class="sxs-lookup"><span data-stu-id="c5694-125">-Tag</span></span>
<span data-ttu-id="c5694-126">這是一組要用於更新的標記。</span><span class="sxs-lookup"><span data-stu-id="c5694-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5694-127">-作業</span><span class="sxs-lookup"><span data-stu-id="c5694-127">-Operation</span></span>
<span data-ttu-id="c5694-128">更新作業。</span><span class="sxs-lookup"><span data-stu-id="c5694-128">The update operation.</span></span> <span data-ttu-id="c5694-129">選項為合併、取代和刪除。</span><span class="sxs-lookup"><span data-stu-id="c5694-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5694-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c5694-130">-Confirm</span></span>
<span data-ttu-id="c5694-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c5694-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5694-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5694-132">-WhatIf</span></span>
<span data-ttu-id="c5694-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5694-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5694-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5694-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5694-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5694-135">CommonParameters</span></span>
<span data-ttu-id="c5694-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5694-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5694-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5694-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5694-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c5694-138">INPUTS</span></span>

### <span data-ttu-id="c5694-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c5694-139">System.String</span></span>

### <span data-ttu-id="c5694-140">Microsoft.Azure.Commands.Tag.model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="c5694-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="c5694-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c5694-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c5694-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c5694-142">OUTPUTS</span></span>

### <span data-ttu-id="c5694-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="c5694-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="c5694-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c5694-144">NOTES</span></span>

## <span data-ttu-id="c5694-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5694-145">RELATED LINKS</span></span>

[<span data-ttu-id="c5694-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="c5694-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="c5694-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="c5694-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="c5694-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="c5694-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
