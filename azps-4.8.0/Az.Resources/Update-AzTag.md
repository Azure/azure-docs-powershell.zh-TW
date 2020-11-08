---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126246"
---
# <span data-ttu-id="f984b-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="f984b-101">Update-AzTag</span></span>

## <span data-ttu-id="f984b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f984b-102">SYNOPSIS</span></span>

<span data-ttu-id="f984b-103">選擇性地更新資源或訂閱上的一組標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="f984b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f984b-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="f984b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f984b-105">DESCRIPTION</span></span>

<span data-ttu-id="f984b-106">含 **ResourceId** 的 **AzTag** Cmdlet 會有選擇性地更新資源或訂閱上的一組標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="f984b-107">這個作業可讓您取代、合併或選擇性地刪除指定資源或訂閱上的標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="f984b-108">指定的實體在作業結束時，最多可以有50標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="f984b-109">[取代] 選項會以一組新的標記取代整個現有標籤。</span><span class="sxs-lookup"><span data-stu-id="f984b-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="f984b-110">[合併] 選項可讓您使用新名稱新增標記，並更新現有名稱的標記值。</span><span class="sxs-lookup"><span data-stu-id="f984b-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="f984b-111">[刪除] 選項可讓您選擇性地刪除以指定名稱或名稱/值對為基礎的標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="f984b-112">示例</span><span class="sxs-lookup"><span data-stu-id="f984b-112">EXAMPLES</span></span>

### <span data-ttu-id="f984b-113">範例1：選擇性地使用「合併」作業來更新訂閱上的標記集</span><span class="sxs-lookup"><span data-stu-id="f984b-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="f984b-114">這個命令會將訂閱上的一組標記與 {subId} 合併在一起。</span><span class="sxs-lookup"><span data-stu-id="f984b-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="f984b-115">範例2：選擇性地使用「取代」作業來更新訂閱上的一組標記</span><span class="sxs-lookup"><span data-stu-id="f984b-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="f984b-116">這個命令會使用 {subId} Repalces 訂閱上的一組標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="f984b-117">範例3：選擇性地使用 "Delete" 運算來更新訂閱上的標記集</span><span class="sxs-lookup"><span data-stu-id="f984b-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="f984b-118">這個命令會在訂閱上刪除 {subId} 的一組標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="f984b-119">參數</span><span class="sxs-lookup"><span data-stu-id="f984b-119">PARAMETERS</span></span>

### <span data-ttu-id="f984b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f984b-120">-DefaultProfile</span></span>
<span data-ttu-id="f984b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f984b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f984b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f984b-122">-ResourceId</span></span>
<span data-ttu-id="f984b-123">標籤實體的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f984b-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="f984b-124">資源、資源群組或訂閱可能會加上標籤。</span><span class="sxs-lookup"><span data-stu-id="f984b-124">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="f984b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f984b-125">-Tag</span></span>
<span data-ttu-id="f984b-126">要用來進行更新的一組標記。</span><span class="sxs-lookup"><span data-stu-id="f984b-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="f984b-127">-操作</span><span class="sxs-lookup"><span data-stu-id="f984b-127">-Operation</span></span>
<span data-ttu-id="f984b-128">更新操作。</span><span class="sxs-lookup"><span data-stu-id="f984b-128">The update operation.</span></span> <span data-ttu-id="f984b-129">選項包括 [合併]、[取代] 和 [刪除]。</span><span class="sxs-lookup"><span data-stu-id="f984b-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f984b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f984b-130">-Confirm</span></span>
<span data-ttu-id="f984b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f984b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f984b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f984b-132">-WhatIf</span></span>
<span data-ttu-id="f984b-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f984b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f984b-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f984b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f984b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f984b-135">CommonParameters</span></span>
<span data-ttu-id="f984b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f984b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f984b-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f984b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f984b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f984b-138">INPUTS</span></span>

### <span data-ttu-id="f984b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f984b-139">System.String</span></span>

### <span data-ttu-id="f984b-140">[TagPatchOpeation] 命令。</span><span class="sxs-lookup"><span data-stu-id="f984b-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="f984b-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f984b-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f984b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f984b-142">OUTPUTS</span></span>

### <span data-ttu-id="f984b-143">[PSTagResource] 命令。</span><span class="sxs-lookup"><span data-stu-id="f984b-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="f984b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f984b-144">NOTES</span></span>

## <span data-ttu-id="f984b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f984b-145">RELATED LINKS</span></span>

[<span data-ttu-id="f984b-146">AzTag</span><span class="sxs-lookup"><span data-stu-id="f984b-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="f984b-147">新-AzTag</span><span class="sxs-lookup"><span data-stu-id="f984b-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="f984b-148">移除-AzTag</span><span class="sxs-lookup"><span data-stu-id="f984b-148">Remove-AzTag</span></span>](./Remove-AzTag.md)