---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 028489985ff7f2c6054ffe3a7b66e94823573356
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903918"
---
# <span data-ttu-id="857d3-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="857d3-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="857d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="857d3-102">SYNOPSIS</span></span>
<span data-ttu-id="857d3-103">以遞迴的方法更新指定路徑上的 ACL。</span><span class="sxs-lookup"><span data-stu-id="857d3-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="857d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="857d3-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="857d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="857d3-105">DESCRIPTION</span></span>
<span data-ttu-id="857d3-106">**Update-AzDataLakeGen2AclRecursive** Cmdlet 會以遞迴的方法更新指定路徑上的 ACL。</span><span class="sxs-lookup"><span data-stu-id="857d3-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="857d3-107">輸入 ACL 會合並原始的 ACL：如果具有相同 AccessControlType/EntityId/DefaultScope 的 ACL 專案存在，請更新許可權;否則會新增 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="857d3-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="857d3-108">例子</span><span class="sxs-lookup"><span data-stu-id="857d3-108">EXAMPLES</span></span>

### <span data-ttu-id="857d3-109">範例 1：在檔案系統的根 directiry 上更新 ACL 遞迴</span><span class="sxs-lookup"><span data-stu-id="857d3-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="857d3-110">此命令會先建立一個包含 3 個 acl 專案之 ACL 物件，然後在檔案系統的根目錄上以遞迴的方法更新 ACL。</span><span class="sxs-lookup"><span data-stu-id="857d3-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="857d3-111">範例 2：更新目錄中的 ACL 遞迴，然後使用 ContinuationToken 從失敗中繼續</span><span class="sxs-lookup"><span data-stu-id="857d3-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="857d3-112">此命令會先將 ACL 遞迴更新至目錄並失敗，然後在使用者修正失敗檔案之後，使用 ContinuationToken 繼續。</span><span class="sxs-lookup"><span data-stu-id="857d3-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="857d3-113">範例 3：更新 ACL 遞迴區塊</span><span class="sxs-lookup"><span data-stu-id="857d3-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="857d3-114">此腳本會以 BatchSize \* MaxBatchCount 的區塊大小，以遞迴的目錄區塊更新 ACL。</span><span class="sxs-lookup"><span data-stu-id="857d3-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="857d3-115">此腳本中的區塊大小為 5000。</span><span class="sxs-lookup"><span data-stu-id="857d3-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="857d3-116">範例 4：在目錄和 ContinueOnFailure 上更新 ACL 遞迴，然後從失敗中一一繼續</span><span class="sxs-lookup"><span data-stu-id="857d3-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="857d3-117">此命令會先以 ContinueOnFailure 將 ACL 遞迴更新至目錄，而有些專案失敗，然後再一個一個繼續失敗的專案。</span><span class="sxs-lookup"><span data-stu-id="857d3-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="857d3-118">參數</span><span class="sxs-lookup"><span data-stu-id="857d3-118">PARAMETERS</span></span>

### <span data-ttu-id="857d3-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="857d3-119">-Acl</span></span>
<span data-ttu-id="857d3-120">POSIX 存取控制清單可針對檔案或目錄設定遞迴。</span><span class="sxs-lookup"><span data-stu-id="857d3-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857d3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="857d3-121">-AsJob</span></span>
<span data-ttu-id="857d3-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="857d3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="857d3-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="857d3-123">-BatchSize</span></span>
<span data-ttu-id="857d3-124">如果資料集大小超過批次大小，則作業會分割成多個要求，以便追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="857d3-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="857d3-125">批次大小應該介於 1 到 2000 之間。</span><span class="sxs-lookup"><span data-stu-id="857d3-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="857d3-126">預設值為 2000。</span><span class="sxs-lookup"><span data-stu-id="857d3-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857d3-127">-內容</span><span class="sxs-lookup"><span data-stu-id="857d3-127">-Context</span></span>
<span data-ttu-id="857d3-128">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="857d3-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="857d3-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="857d3-129">-ContinuationToken</span></span>
<span data-ttu-id="857d3-130">延續權杖。</span><span class="sxs-lookup"><span data-stu-id="857d3-130">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857d3-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="857d3-131">-ContinueOnFailure</span></span>
<span data-ttu-id="857d3-132">將此參數設定為忽略失敗，並繼續進行目錄其他子實體上的作業。</span><span class="sxs-lookup"><span data-stu-id="857d3-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="857d3-133">預設作業在遇到失敗時會快速終止。</span><span class="sxs-lookup"><span data-stu-id="857d3-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="857d3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857d3-134">-DefaultProfile</span></span>
<span data-ttu-id="857d3-135">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="857d3-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857d3-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="857d3-136">-FileSystem</span></span>
<span data-ttu-id="857d3-137">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="857d3-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="857d3-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="857d3-138">-MaxBatchCount</span></span>
<span data-ttu-id="857d3-139">單一變更存取控制作業可以執行的批次數上限。</span><span class="sxs-lookup"><span data-stu-id="857d3-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="857d3-140">如果資料集大小超過 MaxBatchCount 乘 BatchSize，將會返回延續權杖。</span><span class="sxs-lookup"><span data-stu-id="857d3-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857d3-141">-路徑</span><span class="sxs-lookup"><span data-stu-id="857d3-141">-Path</span></span>
<span data-ttu-id="857d3-142">指定 FileSystem 中以遞迴方法變更 Acl 的路徑。</span><span class="sxs-lookup"><span data-stu-id="857d3-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="857d3-143">可以是檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="857d3-143">Can be a file or directory.</span></span>
<span data-ttu-id="857d3-144">在格式為 'directory/file.txt' 或 'directory1/directory2/'。</span><span class="sxs-lookup"><span data-stu-id="857d3-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="857d3-145">跳過設定此參數，以從檔案系統的根目錄以遞迴的方法變更 Acl。</span><span class="sxs-lookup"><span data-stu-id="857d3-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="857d3-146">-確認</span><span class="sxs-lookup"><span data-stu-id="857d3-146">-Confirm</span></span>
<span data-ttu-id="857d3-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="857d3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857d3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857d3-148">-WhatIf</span></span>
<span data-ttu-id="857d3-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="857d3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857d3-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="857d3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857d3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857d3-151">CommonParameters</span></span>
<span data-ttu-id="857d3-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="857d3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857d3-153">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="857d3-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857d3-154">輸入</span><span class="sxs-lookup"><span data-stu-id="857d3-154">INPUTS</span></span>

### <span data-ttu-id="857d3-155">System.String</span><span class="sxs-lookup"><span data-stu-id="857d3-155">System.String</span></span>

### <span data-ttu-id="857d3-156">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="857d3-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="857d3-157">輸出</span><span class="sxs-lookup"><span data-stu-id="857d3-157">OUTPUTS</span></span>

### <span data-ttu-id="857d3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="857d3-158">System.String</span></span>

## <span data-ttu-id="857d3-159">筆記</span><span class="sxs-lookup"><span data-stu-id="857d3-159">NOTES</span></span>

## <span data-ttu-id="857d3-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="857d3-160">RELATED LINKS</span></span>
