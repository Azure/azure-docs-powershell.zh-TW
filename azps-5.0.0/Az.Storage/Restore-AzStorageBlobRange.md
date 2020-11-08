---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137233"
---
# <span data-ttu-id="9ed94-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="9ed94-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="9ed94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ed94-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed94-103">針對特定的 blob 範圍還原儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9ed94-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="9ed94-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ed94-104">SYNTAX</span></span>

### <span data-ttu-id="9ed94-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="9ed94-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed94-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed94-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed94-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9ed94-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed94-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ed94-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed94-109">**Restore-AzStorageBlobRange** Cmdlet 會針對特定的 blob 範圍，還原儲存空間帳戶中的 blob。</span><span class="sxs-lookup"><span data-stu-id="9ed94-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="9ed94-110">包含開始範圍，而結束範圍會排除在 blob 還原中。</span><span class="sxs-lookup"><span data-stu-id="9ed94-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="9ed94-111">示例</span><span class="sxs-lookup"><span data-stu-id="9ed94-111">EXAMPLES</span></span>

### <span data-ttu-id="9ed94-112">範例1：開始使用特定的 blob 範圍來還原儲存空間帳戶中的 blob</span><span class="sxs-lookup"><span data-stu-id="9ed94-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="9ed94-113">這個命令會先建立2個 blob 範圍，然後開始使用1天前的2個 blob 範圍來還原儲存空間帳戶中的 blob。</span><span class="sxs-lookup"><span data-stu-id="9ed94-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="9ed94-114">使用者稍後可以使用 Get-AzStorageAccount 追蹤還原狀態。</span><span class="sxs-lookup"><span data-stu-id="9ed94-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="9ed94-115">範例2：在後端中還原儲存空間帳戶中的所有 blob</span><span class="sxs-lookup"><span data-stu-id="9ed94-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="9ed94-116">這個命令會從30分鐘前還原儲存空間帳戶中的所有 blob，並等待還原完成。</span><span class="sxs-lookup"><span data-stu-id="9ed94-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="9ed94-117">因為還原 blob 可能需要花很長的時間，請在具有 Asjob 參數的後端執行它，然後等待工作完成，並顯示結果。</span><span class="sxs-lookup"><span data-stu-id="9ed94-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="9ed94-118">範例3：直接透過輸入 blob 範圍復原 blob，並等待完成</span><span class="sxs-lookup"><span data-stu-id="9ed94-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="9ed94-119">這個命令會從1天前還原儲存空間帳戶中的 blob （依輸入 2 blob 直接移至 Restore-AzStorageBlobRange Cmdlet）。</span><span class="sxs-lookup"><span data-stu-id="9ed94-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="9ed94-120">這個命令會等到還原完成為止。</span><span class="sxs-lookup"><span data-stu-id="9ed94-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="9ed94-121">參數</span><span class="sxs-lookup"><span data-stu-id="9ed94-121">PARAMETERS</span></span>

### <span data-ttu-id="9ed94-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ed94-122">-AsJob</span></span>
<span data-ttu-id="9ed94-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ed94-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ed94-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="9ed94-124">-BlobRestoreRange</span></span>
<span data-ttu-id="9ed94-125">要還原的 blob 範圍。</span><span class="sxs-lookup"><span data-stu-id="9ed94-125">The blob range to Restore.</span></span>
<span data-ttu-id="9ed94-126">如果未指定此參數，將會還原所有 blob。</span><span class="sxs-lookup"><span data-stu-id="9ed94-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="9ed94-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed94-127">-DefaultProfile</span></span>
<span data-ttu-id="9ed94-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ed94-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed94-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed94-129">-ResourceGroupName</span></span>
<span data-ttu-id="9ed94-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed94-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ed94-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed94-131">-ResourceId</span></span>
<span data-ttu-id="9ed94-132">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ed94-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="9ed94-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ed94-133">-StorageAccount</span></span>
<span data-ttu-id="9ed94-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9ed94-134">Storage account object</span></span>

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

### <span data-ttu-id="9ed94-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9ed94-135">-StorageAccountName</span></span>
<span data-ttu-id="9ed94-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed94-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="9ed94-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="9ed94-137">-TimeToRestore</span></span>
<span data-ttu-id="9ed94-138">還原 Blob 的時間。</span><span class="sxs-lookup"><span data-stu-id="9ed94-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="9ed94-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9ed94-139">-WaitForComplete</span></span>
<span data-ttu-id="9ed94-140">等待還原工作完成</span><span class="sxs-lookup"><span data-stu-id="9ed94-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="9ed94-141">-確認</span><span class="sxs-lookup"><span data-stu-id="9ed94-141">-Confirm</span></span>
<span data-ttu-id="9ed94-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ed94-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed94-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed94-143">-WhatIf</span></span>
<span data-ttu-id="9ed94-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ed94-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ed94-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ed94-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed94-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed94-146">CommonParameters</span></span>
<span data-ttu-id="9ed94-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ed94-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed94-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ed94-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed94-149">輸入</span><span class="sxs-lookup"><span data-stu-id="9ed94-149">INPUTS</span></span>

### <span data-ttu-id="9ed94-150">System.object</span><span class="sxs-lookup"><span data-stu-id="9ed94-150">System.String</span></span>

### <span data-ttu-id="9ed94-151">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9ed94-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9ed94-152">輸出</span><span class="sxs-lookup"><span data-stu-id="9ed94-152">OUTPUTS</span></span>

### <span data-ttu-id="9ed94-153">PSBlobRestoreStatus 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9ed94-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="9ed94-154">筆記</span><span class="sxs-lookup"><span data-stu-id="9ed94-154">NOTES</span></span>

## <span data-ttu-id="9ed94-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ed94-155">RELATED LINKS</span></span>
