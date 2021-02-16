---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136874"
---
# <span data-ttu-id="23235-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="23235-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="23235-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23235-102">SYNOPSIS</span></span>
<span data-ttu-id="23235-103">在指定的路徑上以遞迴方式移除 ACL。</span><span class="sxs-lookup"><span data-stu-id="23235-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="23235-104">句法</span><span class="sxs-lookup"><span data-stu-id="23235-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23235-105">說明</span><span class="sxs-lookup"><span data-stu-id="23235-105">DESCRIPTION</span></span>
<span data-ttu-id="23235-106">**AzDataLakeGen2AclRecursive** Cmdlet 會在指定的路徑上以遞迴方式移除 ACL。</span><span class="sxs-lookup"><span data-stu-id="23235-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="23235-107">原始 ACL 中的 ACL 專案（包含相同的 AccessControlType、DefaultScope 和 EntityId）輸入 ACL (專案，即使 lbe 移除不同的許可權) 。</span><span class="sxs-lookup"><span data-stu-id="23235-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="23235-108">示例</span><span class="sxs-lookup"><span data-stu-id="23235-108">EXAMPLES</span></span>

### <span data-ttu-id="23235-109">範例1：在 filesystem 的根 directiry 上遞迴移除 ACL</span><span class="sxs-lookup"><span data-stu-id="23235-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="23235-110">這個命令會先建立一個具有2個 acl 專案的 ACL 物件，然後在檔案系統的根目錄上以遞迴方式移除 ACL。</span><span class="sxs-lookup"><span data-stu-id="23235-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="23235-111">範例2：在目錄上遞迴移除 ACL</span><span class="sxs-lookup"><span data-stu-id="23235-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

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

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="23235-112">這個命令會先在目錄上遞迴移除 ACL 並失敗，然後在使用者修正失敗的檔案之後，繼續使用 ContinuationToken。</span><span class="sxs-lookup"><span data-stu-id="23235-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="23235-113">範例3：以分塊方式將 ACL 移除成遞迴區塊</span><span class="sxs-lookup"><span data-stu-id="23235-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="23235-114">此腳本會透過區塊移除目錄區塊上的 ACL rescursively，區塊大小為 BatchSize \* MaxBatchCount。</span><span class="sxs-lookup"><span data-stu-id="23235-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="23235-115">此腳本中的組塊大小為50000。</span><span class="sxs-lookup"><span data-stu-id="23235-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="23235-116">範例4：在目錄和 ContinueOnFailure 上遞迴移除 ACL，然後從失敗逐一繼續</span><span class="sxs-lookup"><span data-stu-id="23235-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="23235-117">這個命令會先以 ContinueOnFailure 的方式遞迴移除 ACL，有些專案會失敗，然後逐個繼續失敗的專案。</span><span class="sxs-lookup"><span data-stu-id="23235-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="23235-118">參數</span><span class="sxs-lookup"><span data-stu-id="23235-118">PARAMETERS</span></span>

### <span data-ttu-id="23235-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="23235-119">-Acl</span></span>
<span data-ttu-id="23235-120">[POSIX 存取控制清單]，以遞迴方式設定檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="23235-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="23235-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23235-121">-AsJob</span></span>
<span data-ttu-id="23235-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="23235-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23235-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="23235-123">-BatchSize</span></span>
<span data-ttu-id="23235-124">如果資料集大小超過批大小，則會將操作分割成多個要求，以便追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="23235-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="23235-125">批次大小應該介於1與2000之間。</span><span class="sxs-lookup"><span data-stu-id="23235-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="23235-126">預設值為2000。</span><span class="sxs-lookup"><span data-stu-id="23235-126">Default is 2000.</span></span>

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

### <span data-ttu-id="23235-127">-內容</span><span class="sxs-lookup"><span data-stu-id="23235-127">-Context</span></span>
<span data-ttu-id="23235-128">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="23235-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="23235-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="23235-129">-ContinuationToken</span></span>
<span data-ttu-id="23235-130">延續標記。</span><span class="sxs-lookup"><span data-stu-id="23235-130">Continuation Token.</span></span>

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

### <span data-ttu-id="23235-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="23235-131">-ContinueOnFailure</span></span>
<span data-ttu-id="23235-132">將此參數設定為 [忽略失敗]，並在目錄的其他子實體上繼續 proceeing 操作。</span><span class="sxs-lookup"><span data-stu-id="23235-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="23235-133">預設，此操作將在遇到失敗時快速結束。</span><span class="sxs-lookup"><span data-stu-id="23235-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="23235-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23235-134">-DefaultProfile</span></span>
<span data-ttu-id="23235-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23235-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23235-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="23235-136">-FileSystem</span></span>
<span data-ttu-id="23235-137">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="23235-137">FileSystem name</span></span>

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

### <span data-ttu-id="23235-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="23235-138">-MaxBatchCount</span></span>
<span data-ttu-id="23235-139">可執行單一變更存取控制作業的批次數目上限。</span><span class="sxs-lookup"><span data-stu-id="23235-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="23235-140">如果資料集大小超過 MaxBatchCount 乘以 BatchSize，則會傳回延續標記。</span><span class="sxs-lookup"><span data-stu-id="23235-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="23235-141">-Path</span><span class="sxs-lookup"><span data-stu-id="23235-141">-Path</span></span>
<span data-ttu-id="23235-142">指定的 FileSystem 中要以遞迴方式變更 Acl 的路徑。</span><span class="sxs-lookup"><span data-stu-id="23235-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="23235-143">可以是檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="23235-143">Can be a file or directory.</span></span>
<span data-ttu-id="23235-144">在 [目錄/file.txt] 或 "directory1/directory2/" 格式中。</span><span class="sxs-lookup"><span data-stu-id="23235-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="23235-145">[略過設定此參數] 可從 Filesystem 的根目錄遞迴變更 Acl。</span><span class="sxs-lookup"><span data-stu-id="23235-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="23235-146">-確認</span><span class="sxs-lookup"><span data-stu-id="23235-146">-Confirm</span></span>
<span data-ttu-id="23235-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23235-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23235-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23235-148">-WhatIf</span></span>
<span data-ttu-id="23235-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23235-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23235-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23235-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23235-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23235-151">CommonParameters</span></span>
<span data-ttu-id="23235-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23235-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23235-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23235-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23235-154">輸入</span><span class="sxs-lookup"><span data-stu-id="23235-154">INPUTS</span></span>

### <span data-ttu-id="23235-155">System.object</span><span class="sxs-lookup"><span data-stu-id="23235-155">System.String</span></span>

### <span data-ttu-id="23235-156">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="23235-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="23235-157">輸出</span><span class="sxs-lookup"><span data-stu-id="23235-157">OUTPUTS</span></span>

### <span data-ttu-id="23235-158">System.object</span><span class="sxs-lookup"><span data-stu-id="23235-158">System.String</span></span>

## <span data-ttu-id="23235-159">筆記</span><span class="sxs-lookup"><span data-stu-id="23235-159">NOTES</span></span>

## <span data-ttu-id="23235-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="23235-160">RELATED LINKS</span></span>
