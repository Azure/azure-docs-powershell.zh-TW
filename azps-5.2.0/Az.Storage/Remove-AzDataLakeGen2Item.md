---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273676"
---
# <span data-ttu-id="cf108-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cf108-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="cf108-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf108-102">SYNOPSIS</span></span>
<span data-ttu-id="cf108-103">移除檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="cf108-103">Remove a file or directory.</span></span>

## <span data-ttu-id="cf108-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf108-104">SYNTAX</span></span>

### <span data-ttu-id="cf108-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="cf108-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf108-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="cf108-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf108-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf108-107">DESCRIPTION</span></span>
<span data-ttu-id="cf108-108">**AzDataLakeGen2Item** Cmdlet 會從儲存空間帳戶中移除檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="cf108-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="cf108-109">這個 Cmdlet 只有在已針對儲存空間帳戶啟用階層命名空間時才適用。</span><span class="sxs-lookup"><span data-stu-id="cf108-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="cf108-110">此類型的帳戶可使用「-EnableHierarchicalNamespace $true」執行「新-AzStorageAccount」 Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="cf108-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="cf108-111">示例</span><span class="sxs-lookup"><span data-stu-id="cf108-111">EXAMPLES</span></span>

### <span data-ttu-id="cf108-112">範例1：移除目錄</span><span class="sxs-lookup"><span data-stu-id="cf108-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="cf108-113">這個命令會從 Filesystem 中移除目錄。</span><span class="sxs-lookup"><span data-stu-id="cf108-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="cf108-114">範例2：移除檔案而不出現提示</span><span class="sxs-lookup"><span data-stu-id="cf108-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="cf108-115">這個命令會從 Filesystem 中移除目錄，而不會出現提示。</span><span class="sxs-lookup"><span data-stu-id="cf108-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="cf108-116">範例3：移除具有管線的 Filesystem 中的所有專案</span><span class="sxs-lookup"><span data-stu-id="cf108-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="cf108-117">這個命令會移除具有管線的 Filesystem 中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="cf108-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="cf108-118">參數</span><span class="sxs-lookup"><span data-stu-id="cf108-118">PARAMETERS</span></span>

### <span data-ttu-id="cf108-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf108-119">-AsJob</span></span>
<span data-ttu-id="cf108-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf108-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf108-121">-內容</span><span class="sxs-lookup"><span data-stu-id="cf108-121">-Context</span></span>
<span data-ttu-id="cf108-122">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="cf108-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="cf108-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf108-123">-DefaultProfile</span></span>
<span data-ttu-id="cf108-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf108-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf108-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="cf108-125">-FileSystem</span></span>
<span data-ttu-id="cf108-126">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="cf108-126">FileSystem name</span></span>

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

### <span data-ttu-id="cf108-127">-Force</span><span class="sxs-lookup"><span data-stu-id="cf108-127">-Force</span></span>
<span data-ttu-id="cf108-128">強制移除檔案系統及其所有內容</span><span class="sxs-lookup"><span data-stu-id="cf108-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="cf108-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf108-129">-InputObject</span></span>
<span data-ttu-id="cf108-130">要移除的 Azure Datalake Gen2 Item 物件。</span><span class="sxs-lookup"><span data-stu-id="cf108-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="cf108-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf108-131">-PassThru</span></span>
<span data-ttu-id="cf108-132">返回是否已成功移除指定的 Filesystem</span><span class="sxs-lookup"><span data-stu-id="cf108-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="cf108-133">-Path</span><span class="sxs-lookup"><span data-stu-id="cf108-133">-Path</span></span>
<span data-ttu-id="cf108-134">要移除的指定檔案系統中的路徑。</span><span class="sxs-lookup"><span data-stu-id="cf108-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="cf108-135">可以是 "directory/file.txt" 格式或 "directory1/directory2/" 格式的檔案或目錄</span><span class="sxs-lookup"><span data-stu-id="cf108-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="cf108-136">-確認</span><span class="sxs-lookup"><span data-stu-id="cf108-136">-Confirm</span></span>
<span data-ttu-id="cf108-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf108-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf108-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf108-138">-WhatIf</span></span>
<span data-ttu-id="cf108-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf108-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf108-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf108-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf108-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf108-141">CommonParameters</span></span>
<span data-ttu-id="cf108-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf108-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf108-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf108-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf108-144">輸入</span><span class="sxs-lookup"><span data-stu-id="cf108-144">INPUTS</span></span>

### <span data-ttu-id="cf108-145">System.object</span><span class="sxs-lookup"><span data-stu-id="cf108-145">System.String</span></span>

### <span data-ttu-id="cf108-146">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="cf108-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="cf108-147">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="cf108-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cf108-148">輸出</span><span class="sxs-lookup"><span data-stu-id="cf108-148">OUTPUTS</span></span>

### <span data-ttu-id="cf108-149">System.object</span><span class="sxs-lookup"><span data-stu-id="cf108-149">System.Boolean</span></span>

## <span data-ttu-id="cf108-150">筆記</span><span class="sxs-lookup"><span data-stu-id="cf108-150">NOTES</span></span>

## <span data-ttu-id="cf108-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf108-151">RELATED LINKS</span></span>
