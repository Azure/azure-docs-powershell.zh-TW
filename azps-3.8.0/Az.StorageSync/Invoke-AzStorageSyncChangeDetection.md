---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959076"
---
# <span data-ttu-id="e8639-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="e8639-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="e8639-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8639-102">SYNOPSIS</span></span>
<span data-ttu-id="e8639-103">這個命令可以用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="e8639-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="e8639-104">您可以將它設定為整個共用、子資料夾或一組檔案的目標。</span><span class="sxs-lookup"><span data-stu-id="e8639-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="e8639-105">最多可檢測到10000個專案。</span><span class="sxs-lookup"><span data-stu-id="e8639-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="e8639-106">如果您知道變更的範圍，請將此命令的執行限制在命名空間的各個部分，因此變更偵測可以在10000專案限制內快速完成。</span><span class="sxs-lookup"><span data-stu-id="e8639-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="e8639-107">Invoke-AzStorageSyncChangeDetection Cmdlet 不會偵測到 Azure 檔案共用中刪除的檔案。</span><span class="sxs-lookup"><span data-stu-id="e8639-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="e8639-108">如果檔案已在 Azure 檔案共用中刪除，則會在執行 [變更偵測作業](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) 時偵測到這些檔案。</span><span class="sxs-lookup"><span data-stu-id="e8639-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="e8639-109">句法</span><span class="sxs-lookup"><span data-stu-id="e8639-109">SYNTAX</span></span>

### <span data-ttu-id="e8639-110">StringAndDirectoryParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8639-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8639-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8639-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8639-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8639-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8639-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8639-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8639-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8639-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8639-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8639-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8639-116">說明</span><span class="sxs-lookup"><span data-stu-id="e8639-116">DESCRIPTION</span></span>
<span data-ttu-id="e8639-117">Azure 檔案同步處理會定期檢查同步處理 Azure 檔案共用中的命名空間，以取得與同步處理之外的其他方法所帶來的變更。目標是識別這些變更，並最終將它們同步處理到已連線的伺服器。</span><span class="sxs-lookup"><span data-stu-id="e8639-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="e8639-118">這個命令可以用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="e8639-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="e8639-119">您可以將它設定為整個共用、子資料夾或一組檔案的目標。</span><span class="sxs-lookup"><span data-stu-id="e8639-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="e8639-120">如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。</span><span class="sxs-lookup"><span data-stu-id="e8639-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="e8639-121">示例</span><span class="sxs-lookup"><span data-stu-id="e8639-121">EXAMPLES</span></span>

### <span data-ttu-id="e8639-122">範例1</span><span class="sxs-lookup"><span data-stu-id="e8639-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="e8639-123">在這個範例中，變更偵測會在同步處理 Azure 檔案共用的「資料」和「Reporting\Templates」目錄中執行。</span><span class="sxs-lookup"><span data-stu-id="e8639-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="e8639-124">所有路徑都是相對於 Azure 檔案共用命名空間的根。</span><span class="sxs-lookup"><span data-stu-id="e8639-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="e8639-125">範例2</span><span class="sxs-lookup"><span data-stu-id="e8639-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="e8639-126">在這個範例中，針對命令呼叫者已知已變更的一組檔案，會執行變更偵測。</span><span class="sxs-lookup"><span data-stu-id="e8639-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="e8639-127">我們的目標是讓 Azure 檔案同步偵測並同步處理這些變更。</span><span class="sxs-lookup"><span data-stu-id="e8639-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="e8639-128">範例3</span><span class="sxs-lookup"><span data-stu-id="e8639-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="e8639-129">在這個範例中，會針對「範例」目錄執行變更偵測，並以遞迴方式檢測子目錄中的變更。</span><span class="sxs-lookup"><span data-stu-id="e8639-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="e8639-130">請記住，此命令可以在自動中止前檢測到10000變更。</span><span class="sxs-lookup"><span data-stu-id="e8639-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="e8639-131">如果您懷疑已發生10000以上的變更，請在命名空間的子元件上執行命令。</span><span class="sxs-lookup"><span data-stu-id="e8639-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="e8639-132">參數</span><span class="sxs-lookup"><span data-stu-id="e8639-132">PARAMETERS</span></span>

### <span data-ttu-id="e8639-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8639-133">-AsJob</span></span>
<span data-ttu-id="e8639-134">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e8639-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8639-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8639-135">-DefaultProfile</span></span>
<span data-ttu-id="e8639-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8639-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8639-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="e8639-137">-DirectoryPath</span></span>
<span data-ttu-id="e8639-138">將執行變更偵測的目錄。</span><span class="sxs-lookup"><span data-stu-id="e8639-138">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8639-139">-InputObject</span></span>
<span data-ttu-id="e8639-140">CloudEndpoint 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="e8639-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8639-141">-Name</span></span>
<span data-ttu-id="e8639-142">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8639-142">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8639-143">-PassThru</span></span>
<span data-ttu-id="e8639-144">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e8639-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e8639-145">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="e8639-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e8639-146">-Path</span><span class="sxs-lookup"><span data-stu-id="e8639-146">-Path</span></span>
<span data-ttu-id="e8639-147">將執行變更偵測的路徑。</span><span class="sxs-lookup"><span data-stu-id="e8639-147">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-148">-Recursive</span><span class="sxs-lookup"><span data-stu-id="e8639-148">-Recursive</span></span>
<span data-ttu-id="e8639-149">指示目錄變更檢測是否為遞迴式。</span><span class="sxs-lookup"><span data-stu-id="e8639-149">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8639-150">-ResourceGroupName</span></span>
<span data-ttu-id="e8639-151">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e8639-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8639-152">-ResourceId</span></span>
<span data-ttu-id="e8639-153">CloudEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8639-153">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e8639-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="e8639-155">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8639-155">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e8639-156">-SyncGroupName</span></span>
<span data-ttu-id="e8639-157">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8639-157">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8639-158">-確認</span><span class="sxs-lookup"><span data-stu-id="e8639-158">-Confirm</span></span>
<span data-ttu-id="e8639-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8639-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8639-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8639-160">-WhatIf</span></span>
<span data-ttu-id="e8639-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8639-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8639-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8639-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8639-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8639-163">CommonParameters</span></span>
<span data-ttu-id="e8639-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8639-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8639-165">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8639-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8639-166">輸入</span><span class="sxs-lookup"><span data-stu-id="e8639-166">INPUTS</span></span>

### <span data-ttu-id="e8639-167">System.object</span><span class="sxs-lookup"><span data-stu-id="e8639-167">System.String</span></span>

### <span data-ttu-id="e8639-168">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="e8639-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e8639-169">輸出</span><span class="sxs-lookup"><span data-stu-id="e8639-169">OUTPUTS</span></span>

### <span data-ttu-id="e8639-170">System.void</span><span class="sxs-lookup"><span data-stu-id="e8639-170">System.Void</span></span>

## <span data-ttu-id="e8639-171">筆記</span><span class="sxs-lookup"><span data-stu-id="e8639-171">NOTES</span></span>

## <span data-ttu-id="e8639-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8639-172">RELATED LINKS</span></span>
