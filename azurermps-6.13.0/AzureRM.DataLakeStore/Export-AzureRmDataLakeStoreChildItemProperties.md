---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
ms.openlocfilehash: faaf8a0c614a1243a3e3812cd0b6e1202cc7e75b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451220"
---
# <span data-ttu-id="e0c61-101">Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="e0c61-101">Export-AzureRmDataLakeStoreChildItemProperties</span></span>

## <span data-ttu-id="e0c61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0c61-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c61-103">從指定路徑將整個樹狀結構的 [磁片使用量] 與 [Acl)  (的內容匯出至輸出路徑</span><span class="sxs-lookup"><span data-stu-id="e0c61-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a ouput path</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0c61-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0c61-104">SYNTAX</span></span>

### <span data-ttu-id="e0c61-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="e0c61-105">GetDiskUsage</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0c61-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="e0c61-106">GetAllProperties</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0c61-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="e0c61-107">GetAclDump</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0c61-108">說明</span><span class="sxs-lookup"><span data-stu-id="e0c61-108">DESCRIPTION</span></span>
<span data-ttu-id="e0c61-109">**Export-AzureRmDataLakeStoreChildItemProperties** 是用來報告指定目錄的 ADLS 空間使用量或/和 ACL 使用量，以及它是子目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="e0c61-109">The **Export-AzureRmDataLakeStoreChildItemProperties** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="e0c61-110">示例</span><span class="sxs-lookup"><span data-stu-id="e0c61-110">EXAMPLES</span></span>

### <span data-ttu-id="e0c61-111">範例1：取得所有子目錄和檔案的磁片使用量與 ACL 使用量</span><span class="sxs-lookup"><span data-stu-id="e0c61-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="e0c61-112">取得/a. 下所有子目錄和檔案的磁片使用量和 ACL 使用量</span><span class="sxs-lookup"><span data-stu-id="e0c61-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="e0c61-113">IncludeFile 可確保針對檔案同時報告使用方式</span><span class="sxs-lookup"><span data-stu-id="e0c61-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="e0c61-114">範例2：在隱藏 ACL 隱藏的情況下，取得所有子目錄和檔案的 ACL 使用量</span><span class="sxs-lookup"><span data-stu-id="e0c61-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzureRmDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="e0c61-115">取得/a. 下所有子目錄和檔案的 ACL 使用量</span><span class="sxs-lookup"><span data-stu-id="e0c61-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="e0c61-116">IncludeFile 可確保針對檔案也會報告使用方式。</span><span class="sxs-lookup"><span data-stu-id="e0c61-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="e0c61-117">在此情況下，HideconsistentAcl 會顯示/a 的 Acl （而不是其子項），因為所有子系都有與/a. 相同的 acl。</span><span class="sxs-lookup"><span data-stu-id="e0c61-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="e0c61-118">如果您的所有 acl 都與根目錄相同，此旗標會跳過子樹的 acl 輸出。</span><span class="sxs-lookup"><span data-stu-id="e0c61-118">This flag skips the acl ouput of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="e0c61-119">參數</span><span class="sxs-lookup"><span data-stu-id="e0c61-119">PARAMETERS</span></span>

### <span data-ttu-id="e0c61-120">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e0c61-120">-Account</span></span>
<span data-ttu-id="e0c61-121">在其中執行 filesystem 操作的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="e0c61-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="e0c61-122">-併發性</span><span class="sxs-lookup"><span data-stu-id="e0c61-122">-Concurrency</span></span>
<span data-ttu-id="e0c61-123">指出並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="e0c61-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="e0c61-124">根據系統規格，會將預設值計算為最大的精力。</span><span class="sxs-lookup"><span data-stu-id="e0c61-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="e0c61-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c61-125">-DefaultProfile</span></span>
<span data-ttu-id="e0c61-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0c61-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c61-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="e0c61-127">-GetAcl</span></span>
<span data-ttu-id="e0c61-128">從根路徑開始檢索 acl</span><span class="sxs-lookup"><span data-stu-id="e0c61-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="e0c61-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="e0c61-129">-GetDiskUsage</span></span>
<span data-ttu-id="e0c61-130">從根路徑開始檢索磁片使用量</span><span class="sxs-lookup"><span data-stu-id="e0c61-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="e0c61-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="e0c61-131">-HideConsistentAcl</span></span>
<span data-ttu-id="e0c61-132">如果 Acl 在整個子樹中都是相同的，請勿顯示目錄子樹。</span><span class="sxs-lookup"><span data-stu-id="e0c61-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="e0c61-133">這可讓您更輕鬆地只看到 Acl 所不相同的路徑。例如，如果/a/b 下的所有檔案和資料夾都是相同的，則不會顯示 subtreeunder/a/b，只要未設定 ColumnCannot，就會設定一致 ACL IncludeFiles 中的 [True]/a/b，因為不需要為檔案建立 acl，就無法判斷一致的 Acl。</span><span class="sxs-lookup"><span data-stu-id="e0c61-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="e0c61-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="e0c61-134">-IncludeFile</span></span>
<span data-ttu-id="e0c61-135">在檔案層級顯示 stats (預設為只顯示目錄層級資訊) </span><span class="sxs-lookup"><span data-stu-id="e0c61-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="e0c61-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="e0c61-136">-MaximumDepth</span></span>
<span data-ttu-id="e0c61-137">在顯示磁片使用量或 acl 之前，根目錄的最大深度</span><span class="sxs-lookup"><span data-stu-id="e0c61-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="e0c61-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e0c61-138">-OutputPath</span></span>
<span data-ttu-id="e0c61-139">輸出檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="e0c61-139">Path to output file.</span></span> <span data-ttu-id="e0c61-140">可以是本機路徑或 Adl 路徑。</span><span class="sxs-lookup"><span data-stu-id="e0c61-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="e0c61-141">預設為本機。</span><span class="sxs-lookup"><span data-stu-id="e0c61-141">By default it is local.</span></span> <span data-ttu-id="e0c61-142">如果 SaveToAdl 是 pecified，則是同一帳戶中的 ADL 路徑</span><span class="sxs-lookup"><span data-stu-id="e0c61-142">If SaveToAdl is pecified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="e0c61-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0c61-143">-PassThru</span></span>
<span data-ttu-id="e0c61-144">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="e0c61-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="e0c61-145">-Path</span><span class="sxs-lookup"><span data-stu-id="e0c61-145">-Path</span></span>
<span data-ttu-id="e0c61-146">指定的資料 Lake 帳戶中應該要檢索的路徑。</span><span class="sxs-lookup"><span data-stu-id="e0c61-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="e0c61-147">可以是 [/folder/file.txt "格式的檔案或資料夾，其中第一個"/"代表了檔案系統的根。</span><span class="sxs-lookup"><span data-stu-id="e0c61-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="e0c61-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="e0c61-148">-SaveToAdl</span></span>
<span data-ttu-id="e0c61-149">如果傳遞，則會將轉儲檔案儲存至 ADL。</span><span class="sxs-lookup"><span data-stu-id="e0c61-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="e0c61-150">在這種情況下，DumpFile 會是 ADL 路徑</span><span class="sxs-lookup"><span data-stu-id="e0c61-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="e0c61-151">-確認</span><span class="sxs-lookup"><span data-stu-id="e0c61-151">-Confirm</span></span>
<span data-ttu-id="e0c61-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0c61-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c61-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c61-153">-WhatIf</span></span>
<span data-ttu-id="e0c61-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0c61-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c61-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0c61-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c61-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c61-156">CommonParameters</span></span>
<span data-ttu-id="e0c61-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0c61-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c61-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0c61-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c61-159">輸入</span><span class="sxs-lookup"><span data-stu-id="e0c61-159">INPUTS</span></span>

### <span data-ttu-id="e0c61-160">System.object</span><span class="sxs-lookup"><span data-stu-id="e0c61-160">System.String</span></span>

### <span data-ttu-id="e0c61-161">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="e0c61-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e0c61-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e0c61-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e0c61-163">System.object</span><span class="sxs-lookup"><span data-stu-id="e0c61-163">System.Int32</span></span>

## <span data-ttu-id="e0c61-164">輸出</span><span class="sxs-lookup"><span data-stu-id="e0c61-164">OUTPUTS</span></span>

### <span data-ttu-id="e0c61-165">System.object</span><span class="sxs-lookup"><span data-stu-id="e0c61-165">System.Boolean</span></span>

## <span data-ttu-id="e0c61-166">筆記</span><span class="sxs-lookup"><span data-stu-id="e0c61-166">NOTES</span></span>

## <span data-ttu-id="e0c61-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0c61-167">RELATED LINKS</span></span>