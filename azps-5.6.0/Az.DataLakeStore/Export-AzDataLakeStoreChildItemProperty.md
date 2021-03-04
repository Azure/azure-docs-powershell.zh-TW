---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917338"
---
# <span data-ttu-id="e580d-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="e580d-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="e580d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e580d-102">SYNOPSIS</span></span>
<span data-ttu-id="e580d-103">匯出 (磁片使用量和 Acl) 從指定路徑匯出至輸出路徑的整個樹狀結構</span><span class="sxs-lookup"><span data-stu-id="e580d-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="e580d-104">語法</span><span class="sxs-lookup"><span data-stu-id="e580d-104">SYNTAX</span></span>

### <span data-ttu-id="e580d-105">Get讓Usage</span><span class="sxs-lookup"><span data-stu-id="e580d-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e580d-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="e580d-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e580d-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="e580d-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e580d-108">描述</span><span class="sxs-lookup"><span data-stu-id="e580d-108">DESCRIPTION</span></span>
<span data-ttu-id="e580d-109">**Export-AzDataLakeStoreChildItemProperty** 是用來報告指定的目錄及其子目錄和檔案的 ADLS 空間使用量或/和 ACL 使用量。</span><span class="sxs-lookup"><span data-stu-id="e580d-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="e580d-110">例子</span><span class="sxs-lookup"><span data-stu-id="e580d-110">EXAMPLES</span></span>

### <span data-ttu-id="e580d-111">範例 1：取得所有子目錄和檔案的磁片使用量和 ACL 使用量</span><span class="sxs-lookup"><span data-stu-id="e580d-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="e580d-112">取得 /a 下所有子目錄和檔案的磁片使用量和 ACL 使用量。</span><span class="sxs-lookup"><span data-stu-id="e580d-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="e580d-113">IncludeFile 可確保系統同時報告檔案使用量</span><span class="sxs-lookup"><span data-stu-id="e580d-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="e580d-114">範例 2：取得隱藏一致 ACL 的所有子目錄和檔案的 ACL 使用量</span><span class="sxs-lookup"><span data-stu-id="e580d-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="e580d-115">取得 /a 下所有子目錄和檔案的 ACL 使用量。</span><span class="sxs-lookup"><span data-stu-id="e580d-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="e580d-116">IncludeFile 可確保系統同時報告檔案使用量。</span><span class="sxs-lookup"><span data-stu-id="e580d-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="e580d-117">在此案例中，HideconsistentAcl 會顯示 /a 的 Acl，而不是其子項，因為所有子項都有與 /a 相同的 acl。</span><span class="sxs-lookup"><span data-stu-id="e580d-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="e580d-118">如果子樹的所有 acl 與根目錄相同，此旗標會略過子樹的 acl 輸出。</span><span class="sxs-lookup"><span data-stu-id="e580d-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="e580d-119">參數</span><span class="sxs-lookup"><span data-stu-id="e580d-119">PARAMETERS</span></span>

### <span data-ttu-id="e580d-120">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e580d-120">-Account</span></span>
<span data-ttu-id="e580d-121">Data Lake Store 帳戶以在</span><span class="sxs-lookup"><span data-stu-id="e580d-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-122">-並行</span><span class="sxs-lookup"><span data-stu-id="e580d-122">-Concurrency</span></span>
<span data-ttu-id="e580d-123">表示平行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="e580d-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="e580d-124">根據系統規格，預設會以最佳效果計算。</span><span class="sxs-lookup"><span data-stu-id="e580d-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e580d-125">-DefaultProfile</span></span>
<span data-ttu-id="e580d-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e580d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e580d-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="e580d-127">-GetAcl</span></span>
<span data-ttu-id="e580d-128">從根路徑開始取回 acl</span><span class="sxs-lookup"><span data-stu-id="e580d-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-129">-Get使用Usage</span><span class="sxs-lookup"><span data-stu-id="e580d-129">-GetDiskUsage</span></span>
<span data-ttu-id="e580d-130">從根路徑開始取回磁片使用量</span><span class="sxs-lookup"><span data-stu-id="e580d-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="e580d-131">-HideConsistentAcl</span></span>
<span data-ttu-id="e580d-132">如果整個子樹中的 ACL 都相同，請不要顯示目錄子樹。</span><span class="sxs-lookup"><span data-stu-id="e580d-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="e580d-133">這樣一來，就更容易看到 ACL 差異的路徑。例如，如果 /a/b 下的所有檔案和資料夾都相同，則不要顯示子樹 /a/b，若未設定 IncludeFiles，則只輸出 /a/b 在一致的 ACL 欄中輸入 "True"，就無法設定，因為若未針對檔案取回 acl，就無法判斷一致的 Acl。</span><span class="sxs-lookup"><span data-stu-id="e580d-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="e580d-134">-IncludeFile</span></span>
<span data-ttu-id="e580d-135">在檔案層級顯示 (預設為只顯示目錄層級) </span><span class="sxs-lookup"><span data-stu-id="e580d-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="e580d-136">-MaximumDepth</span></span>
<span data-ttu-id="e580d-137">根目錄的最大深度，直到顯示磁片使用量或 acl 為止</span><span class="sxs-lookup"><span data-stu-id="e580d-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e580d-138">-OutputPath</span></span>
<span data-ttu-id="e580d-139">輸出檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="e580d-139">Path to output file.</span></span> <span data-ttu-id="e580d-140">可以是本地路徑或 Adl 路徑。</span><span class="sxs-lookup"><span data-stu-id="e580d-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="e580d-141">根據預設，它是本地的。</span><span class="sxs-lookup"><span data-stu-id="e580d-141">By default it is local.</span></span> <span data-ttu-id="e580d-142">如果已指定 SaveToAdl，則它是同一個帳戶中的 ADL 路徑</span><span class="sxs-lookup"><span data-stu-id="e580d-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e580d-143">-PassThru</span></span>
<span data-ttu-id="e580d-144">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e580d-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-145">-路徑</span><span class="sxs-lookup"><span data-stu-id="e580d-145">-Path</span></span>
<span data-ttu-id="e580d-146">指定 Data Lake 帳戶中應該要取取的路徑。</span><span class="sxs-lookup"><span data-stu-id="e580d-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="e580d-147">可以是檔案或資料夾，格式為 '/folder/file.txt'，其中 DNS 後的第一個 '/' 代表檔案系統的根目錄。</span><span class="sxs-lookup"><span data-stu-id="e580d-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="e580d-148">-SaveToAdl</span></span>
<span data-ttu-id="e580d-149">如果通過，會將轉儲檔案存到 ADL。</span><span class="sxs-lookup"><span data-stu-id="e580d-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="e580d-150">在這種情況下，DumpFile 會是 ADL 路徑</span><span class="sxs-lookup"><span data-stu-id="e580d-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e580d-151">-確認</span><span class="sxs-lookup"><span data-stu-id="e580d-151">-Confirm</span></span>
<span data-ttu-id="e580d-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e580d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e580d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e580d-153">-WhatIf</span></span>
<span data-ttu-id="e580d-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e580d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e580d-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e580d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e580d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e580d-156">CommonParameters</span></span>
<span data-ttu-id="e580d-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e580d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e580d-158">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e580d-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e580d-159">輸入</span><span class="sxs-lookup"><span data-stu-id="e580d-159">INPUTS</span></span>

### <span data-ttu-id="e580d-160">System.String</span><span class="sxs-lookup"><span data-stu-id="e580d-160">System.String</span></span>

### <span data-ttu-id="e580d-161">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e580d-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e580d-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e580d-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e580d-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e580d-163">System.Int32</span></span>

## <span data-ttu-id="e580d-164">輸出</span><span class="sxs-lookup"><span data-stu-id="e580d-164">OUTPUTS</span></span>

### <span data-ttu-id="e580d-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e580d-165">System.Boolean</span></span>

## <span data-ttu-id="e580d-166">筆記</span><span class="sxs-lookup"><span data-stu-id="e580d-166">NOTES</span></span>

## <span data-ttu-id="e580d-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="e580d-167">RELATED LINKS</span></span>
