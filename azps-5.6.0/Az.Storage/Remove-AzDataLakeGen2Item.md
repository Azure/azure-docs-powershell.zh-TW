---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 2d3db18c49d29cabb8f6459adcd46a9c0242c02f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909414"
---
# <span data-ttu-id="e9752-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e9752-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="e9752-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9752-102">SYNOPSIS</span></span>
<span data-ttu-id="e9752-103">移除檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="e9752-103">Remove a file or directory.</span></span>

## <span data-ttu-id="e9752-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9752-104">SYNTAX</span></span>

### <span data-ttu-id="e9752-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="e9752-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9752-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="e9752-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9752-107">描述</span><span class="sxs-lookup"><span data-stu-id="e9752-107">DESCRIPTION</span></span>
<span data-ttu-id="e9752-108">**Remove-AzDataLakeGen2Item** Cmdlet 會從儲存空間帳戶移除檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="e9752-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="e9752-109">只有在儲存空間帳戶已啟用階層式命名空間時，此 Cmdlet 才能運作。</span><span class="sxs-lookup"><span data-stu-id="e9752-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="e9752-110">這類帳戶可以使用「-EnableHierarchicalNamespace $true」執行「New-AzStorageAccount」Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="e9752-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="e9752-111">例子</span><span class="sxs-lookup"><span data-stu-id="e9752-111">EXAMPLES</span></span>

### <span data-ttu-id="e9752-112">範例 1：移除目錄</span><span class="sxs-lookup"><span data-stu-id="e9752-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="e9752-113">此命令會從檔案系統移除目錄。</span><span class="sxs-lookup"><span data-stu-id="e9752-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="e9752-114">範例 2：移除檔案而不提示</span><span class="sxs-lookup"><span data-stu-id="e9752-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="e9752-115">此命令會從檔案系統移除目錄，而不會提示。</span><span class="sxs-lookup"><span data-stu-id="e9752-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="e9752-116">範例 3：移除檔案系統中具有管線的所有專案</span><span class="sxs-lookup"><span data-stu-id="e9752-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="e9752-117">此命令會移除檔案系統中具有管線的所有專案。</span><span class="sxs-lookup"><span data-stu-id="e9752-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="e9752-118">參數</span><span class="sxs-lookup"><span data-stu-id="e9752-118">PARAMETERS</span></span>

### <span data-ttu-id="e9752-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9752-119">-AsJob</span></span>
<span data-ttu-id="e9752-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9752-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9752-121">-內容</span><span class="sxs-lookup"><span data-stu-id="e9752-121">-Context</span></span>
<span data-ttu-id="e9752-122">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="e9752-122">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9752-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9752-123">-DefaultProfile</span></span>
<span data-ttu-id="e9752-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9752-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9752-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="e9752-125">-FileSystem</span></span>
<span data-ttu-id="e9752-126">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="e9752-126">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9752-127">-強制</span><span class="sxs-lookup"><span data-stu-id="e9752-127">-Force</span></span>
<span data-ttu-id="e9752-128">強制移除檔案系統及其中所有內容</span><span class="sxs-lookup"><span data-stu-id="e9752-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="e9752-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9752-129">-InputObject</span></span>
<span data-ttu-id="e9752-130">要移除的 Azure Datalake Gen2 專案物件。</span><span class="sxs-lookup"><span data-stu-id="e9752-130">Azure Datalake Gen2 Item Object to remove.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9752-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9752-131">-PassThru</span></span>
<span data-ttu-id="e9752-132">返回指定的檔案系統是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="e9752-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="e9752-133">-路徑</span><span class="sxs-lookup"><span data-stu-id="e9752-133">-Path</span></span>
<span data-ttu-id="e9752-134">指定檔案系統中應移除的路徑。</span><span class="sxs-lookup"><span data-stu-id="e9752-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="e9752-135">可以是檔案或目錄，格式為 'directory/file.txt' 或 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="e9752-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9752-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e9752-136">-Confirm</span></span>
<span data-ttu-id="e9752-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e9752-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9752-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9752-138">-WhatIf</span></span>
<span data-ttu-id="e9752-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9752-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9752-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9752-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9752-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9752-141">CommonParameters</span></span>
<span data-ttu-id="e9752-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9752-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9752-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e9752-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9752-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e9752-144">INPUTS</span></span>

### <span data-ttu-id="e9752-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e9752-145">System.String</span></span>

### <span data-ttu-id="e9752-146">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e9752-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="e9752-147">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="e9752-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9752-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e9752-148">OUTPUTS</span></span>

### <span data-ttu-id="e9752-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9752-149">System.Boolean</span></span>

## <span data-ttu-id="e9752-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e9752-150">NOTES</span></span>

## <span data-ttu-id="e9752-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9752-151">RELATED LINKS</span></span>
