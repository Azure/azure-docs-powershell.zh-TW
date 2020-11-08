---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139906"
---
# <span data-ttu-id="8bcc9-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="8bcc9-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="8bcc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8bcc9-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcc9-103">在指定的路徑上以遞迴方式更新 ACL。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="8bcc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="8bcc9-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bcc9-105">說明</span><span class="sxs-lookup"><span data-stu-id="8bcc9-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcc9-106">**更新-AzDataLakeGen2AclRecursive** Cmdlet 會在指定的路徑上以遞迴方式更新 ACL。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="8bcc9-107">輸入 ACL 會合並原始的 ACL：如果存在含相同 AccessControlType/EntityId/DefaultScope 的 ACL 專案，請更新許可權;否則，請新增 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="8bcc9-108">示例</span><span class="sxs-lookup"><span data-stu-id="8bcc9-108">EXAMPLES</span></span>

### <span data-ttu-id="8bcc9-109">範例1：在 filesystem 的根 directiry 上遞迴更新 ACL</span><span class="sxs-lookup"><span data-stu-id="8bcc9-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
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

<span data-ttu-id="8bcc9-110">這個命令會先建立含3個 acl 專案的 ACL 物件，然後以遞迴方式在檔案系統的根目錄上更新 ACL。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="8bcc9-111">範例2：以遞迴方式在目錄上更新 ACL，並無法使用 ContinuationToken 從失敗中繼續</span><span class="sxs-lookup"><span data-stu-id="8bcc9-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
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

<span data-ttu-id="8bcc9-112">這個命令首先會將 ACL updateds 遞迴至目錄並失敗，然後在使用者修正失敗的檔案之後，繼續執行 ContinuationToken。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="8bcc9-113">範例3：以分塊方式將 ACL 更新為遞迴區塊</span><span class="sxs-lookup"><span data-stu-id="8bcc9-113">Example 3: Update ACL recursively chunk by chunk</span></span>
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

<span data-ttu-id="8bcc9-114">此腳本會透過區塊來更新目錄區塊上的 ACL rescursively，區塊大小為 BatchSize \* MaxBatchCount。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="8bcc9-115">此腳本中的組塊大小為5000。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="8bcc9-116">範例4：在目錄和 ContinueOnFailure 上遞迴更新 ACL，然後逐個從失敗繼續</span><span class="sxs-lookup"><span data-stu-id="8bcc9-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
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

<span data-ttu-id="8bcc9-117">這個命令首先會將 ACL updateds 遞迴到具有 ContinueOnFailure 的目錄，而某些專案失敗，然後逐個繼續失敗的專案。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="8bcc9-118">參數</span><span class="sxs-lookup"><span data-stu-id="8bcc9-118">PARAMETERS</span></span>

### <span data-ttu-id="8bcc9-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="8bcc9-119">-Acl</span></span>
<span data-ttu-id="8bcc9-120">[POSIX 存取控制清單]，以遞迴方式設定檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="8bcc9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bcc9-121">-AsJob</span></span>
<span data-ttu-id="8bcc9-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8bcc9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bcc9-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="8bcc9-123">-BatchSize</span></span>
<span data-ttu-id="8bcc9-124">如果資料集大小超過批大小，則會將操作分割成多個要求，以便追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="8bcc9-125">批次大小應該介於1與2000之間。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="8bcc9-126">預設值為2000。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-126">Default is 2000.</span></span>

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

### <span data-ttu-id="8bcc9-127">-內容</span><span class="sxs-lookup"><span data-stu-id="8bcc9-127">-Context</span></span>
<span data-ttu-id="8bcc9-128">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="8bcc9-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8bcc9-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="8bcc9-129">-ContinuationToken</span></span>
<span data-ttu-id="8bcc9-130">延續標記。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-130">Continuation Token.</span></span>

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

### <span data-ttu-id="8bcc9-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="8bcc9-131">-ContinueOnFailure</span></span>
<span data-ttu-id="8bcc9-132">將此參數設定為 [忽略失敗]，並在目錄的其他子實體上繼續 proceeing 操作。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="8bcc9-133">預設，此操作將在遇到失敗時快速結束。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="8bcc9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcc9-134">-DefaultProfile</span></span>
<span data-ttu-id="8bcc9-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcc9-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8bcc9-136">-FileSystem</span></span>
<span data-ttu-id="8bcc9-137">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="8bcc9-137">FileSystem name</span></span>

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

### <span data-ttu-id="8bcc9-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="8bcc9-138">-MaxBatchCount</span></span>
<span data-ttu-id="8bcc9-139">可執行單一變更存取控制作業的批次數目上限。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="8bcc9-140">如果資料集大小超過 MaxBatchCount 乘以 BatchSize，則會傳回延續標記。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="8bcc9-141">-Path</span><span class="sxs-lookup"><span data-stu-id="8bcc9-141">-Path</span></span>
<span data-ttu-id="8bcc9-142">指定的 FileSystem 中要以遞迴方式變更 Acl 的路徑。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="8bcc9-143">可以是檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-143">Can be a file or directory.</span></span>
<span data-ttu-id="8bcc9-144">在 [目錄/file.txt] 或 "directory1/directory2/" 格式中。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="8bcc9-145">[略過設定此參數] 可從 Filesystem 的根目錄遞迴變更 Acl。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="8bcc9-146">-確認</span><span class="sxs-lookup"><span data-stu-id="8bcc9-146">-Confirm</span></span>
<span data-ttu-id="8bcc9-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcc9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcc9-148">-WhatIf</span></span>
<span data-ttu-id="8bcc9-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bcc9-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcc9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcc9-151">CommonParameters</span></span>
<span data-ttu-id="8bcc9-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcc9-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8bcc9-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcc9-154">輸入</span><span class="sxs-lookup"><span data-stu-id="8bcc9-154">INPUTS</span></span>

### <span data-ttu-id="8bcc9-155">System.object</span><span class="sxs-lookup"><span data-stu-id="8bcc9-155">System.String</span></span>

### <span data-ttu-id="8bcc9-156">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="8bcc9-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8bcc9-157">輸出</span><span class="sxs-lookup"><span data-stu-id="8bcc9-157">OUTPUTS</span></span>

### <span data-ttu-id="8bcc9-158">System.object</span><span class="sxs-lookup"><span data-stu-id="8bcc9-158">System.String</span></span>

## <span data-ttu-id="8bcc9-159">筆記</span><span class="sxs-lookup"><span data-stu-id="8bcc9-159">NOTES</span></span>

## <span data-ttu-id="8bcc9-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bcc9-160">RELATED LINKS</span></span>
