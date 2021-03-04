---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: 0d742c257927c06686dc9ce799cdc3e4a5b92340
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917882"
---
# <span data-ttu-id="c76eb-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="c76eb-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="c76eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c76eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c76eb-103">還原特定 Blob 範圍的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c76eb-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="c76eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="c76eb-104">SYNTAX</span></span>

### <span data-ttu-id="c76eb-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="c76eb-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c76eb-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c76eb-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c76eb-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c76eb-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c76eb-108">描述</span><span class="sxs-lookup"><span data-stu-id="c76eb-108">DESCRIPTION</span></span>
<span data-ttu-id="c76eb-109">**Restore-AzStorageBlobRange** Cmdlet 會還原儲存帳戶中特定 Blob 範圍中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="c76eb-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="c76eb-110">包含開始範圍，而 Blob 還原會排除結束範圍。</span><span class="sxs-lookup"><span data-stu-id="c76eb-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="c76eb-111">例子</span><span class="sxs-lookup"><span data-stu-id="c76eb-111">EXAMPLES</span></span>

### <span data-ttu-id="c76eb-112">範例 1：開始還原具有特定 Blob 範圍之儲存體帳戶中的 Blob</span><span class="sxs-lookup"><span data-stu-id="c76eb-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="c76eb-113">此命令會先建立 2 個 Blob 範圍，然後從 1 天前的 2 個 Blob 範圍開始還原儲存帳戶中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="c76eb-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="c76eb-114">使用者可以稍後Get-AzStorageAccount追蹤還原狀態。</span><span class="sxs-lookup"><span data-stu-id="c76eb-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="c76eb-115">範例 2：還原後端中儲存空間帳戶中的所有 Blob</span><span class="sxs-lookup"><span data-stu-id="c76eb-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="c76eb-116">此命令會從 30 分鐘前還原儲存空間帳戶中的所有 Blob，並等待還原完成。</span><span class="sxs-lookup"><span data-stu-id="c76eb-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="c76eb-117">由於還原 Blob 可能需要很長的時間，因此請以 -Asjob 參數在後端執行，然後等待工作完成，然後顯示結果。</span><span class="sxs-lookup"><span data-stu-id="c76eb-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="c76eb-118">範例 3：直接根據輸入 Blob 範圍還原 Blob，並等待完成</span><span class="sxs-lookup"><span data-stu-id="c76eb-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="c76eb-119">此命令會直接從 Cmdlet 輸入 2 個 blob 範圍，以還原儲存Restore-AzStorageBlobRange Blob。</span><span class="sxs-lookup"><span data-stu-id="c76eb-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="c76eb-120">此命令會等待還原完成。</span><span class="sxs-lookup"><span data-stu-id="c76eb-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="c76eb-121">參數</span><span class="sxs-lookup"><span data-stu-id="c76eb-121">PARAMETERS</span></span>

### <span data-ttu-id="c76eb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c76eb-122">-AsJob</span></span>
<span data-ttu-id="c76eb-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c76eb-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c76eb-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="c76eb-124">-BlobRestoreRange</span></span>
<span data-ttu-id="c76eb-125">要還原的 Blob 範圍。</span><span class="sxs-lookup"><span data-stu-id="c76eb-125">The blob range to Restore.</span></span>
<span data-ttu-id="c76eb-126">如果未指定此參數，將會還原所有 Blob。</span><span class="sxs-lookup"><span data-stu-id="c76eb-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76eb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76eb-127">-DefaultProfile</span></span>
<span data-ttu-id="c76eb-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c76eb-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c76eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c76eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="c76eb-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c76eb-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76eb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c76eb-131">-ResourceId</span></span>
<span data-ttu-id="c76eb-132">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c76eb-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76eb-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c76eb-133">-StorageAccount</span></span>
<span data-ttu-id="c76eb-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="c76eb-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c76eb-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c76eb-135">-StorageAccountName</span></span>
<span data-ttu-id="c76eb-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c76eb-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76eb-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="c76eb-137">-TimeToRestore</span></span>
<span data-ttu-id="c76eb-138">還原 Blob 的時間。</span><span class="sxs-lookup"><span data-stu-id="c76eb-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76eb-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="c76eb-139">-WaitForComplete</span></span>
<span data-ttu-id="c76eb-140">等待還原工作完成</span><span class="sxs-lookup"><span data-stu-id="c76eb-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="c76eb-141">-確認</span><span class="sxs-lookup"><span data-stu-id="c76eb-141">-Confirm</span></span>
<span data-ttu-id="c76eb-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c76eb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c76eb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c76eb-143">-WhatIf</span></span>
<span data-ttu-id="c76eb-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c76eb-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c76eb-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c76eb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c76eb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76eb-146">CommonParameters</span></span>
<span data-ttu-id="c76eb-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c76eb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76eb-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c76eb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76eb-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c76eb-149">INPUTS</span></span>

### <span data-ttu-id="c76eb-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c76eb-150">System.String</span></span>

### <span data-ttu-id="c76eb-151">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c76eb-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c76eb-152">輸出</span><span class="sxs-lookup"><span data-stu-id="c76eb-152">OUTPUTS</span></span>

### <span data-ttu-id="c76eb-153">Microsoft.Azure.Commands.management.storage.models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="c76eb-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="c76eb-154">筆記</span><span class="sxs-lookup"><span data-stu-id="c76eb-154">NOTES</span></span>

## <span data-ttu-id="c76eb-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c76eb-155">RELATED LINKS</span></span>
