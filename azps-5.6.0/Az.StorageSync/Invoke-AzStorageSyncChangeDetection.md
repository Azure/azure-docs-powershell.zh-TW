---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: d55ffe30554c70b9d7b8fa1ed90380c6a5b181cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916854"
---
# <span data-ttu-id="c46f7-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="c46f7-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="c46f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c46f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c46f7-103">此命令可用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="c46f7-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c46f7-104">它可以鎖定至整個共用、子資料夾或一組檔案。</span><span class="sxs-lookup"><span data-stu-id="c46f7-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c46f7-105">最多可偵測到 10，000 個專案。</span><span class="sxs-lookup"><span data-stu-id="c46f7-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="c46f7-106">如果您知道變更的範圍，將此命令的執行限制為命名空間的一部分，如此一來，變更偵測就可以在 10，000 個專案限制內快速完成。</span><span class="sxs-lookup"><span data-stu-id="c46f7-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="c46f7-107">Cmdlet Invoke-AzStorageSyncChangeDetection不會偵測到 Azure 檔案共用中的下列變更：</span><span class="sxs-lookup"><span data-stu-id="c46f7-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="c46f7-108">刪除的檔案。</span><span class="sxs-lookup"><span data-stu-id="c46f7-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="c46f7-109">從共用中移開的檔案。</span><span class="sxs-lookup"><span data-stu-id="c46f7-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="c46f7-110">以相同名稱刪除及建立之檔案。</span><span class="sxs-lookup"><span data-stu-id="c46f7-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="c46f7-111">執行變更偵測作業時， [會偵測到這些](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) 變更。</span><span class="sxs-lookup"><span data-stu-id="c46f7-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="c46f7-112">語法</span><span class="sxs-lookup"><span data-stu-id="c46f7-112">SYNTAX</span></span>

### <span data-ttu-id="c46f7-113">StringAndDirectoryParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c46f7-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f7-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f7-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f7-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f7-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f7-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f7-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f7-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f7-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46f7-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46f7-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c46f7-119">描述</span><span class="sxs-lookup"><span data-stu-id="c46f7-119">DESCRIPTION</span></span>
<span data-ttu-id="c46f7-120">Azure 檔案同步管理會定期檢查同步的 Azure 檔案共用中的命名空間，以同步的其他方式檢查進入檔案共用中的變更。目標是找出這些變更，並最終同步處理到連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c46f7-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="c46f7-121">此命令可用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="c46f7-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c46f7-122">它可以鎖定至整個共用、子資料夾或一組檔案。</span><span class="sxs-lookup"><span data-stu-id="c46f7-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c46f7-123">如果您知道變更的範圍，請限制將此命令的執行範圍限制為命名空間的一部分，以便快速完成變更偵測，且在 10，000 個專案限制之內。</span><span class="sxs-lookup"><span data-stu-id="c46f7-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="c46f7-124">例子</span><span class="sxs-lookup"><span data-stu-id="c46f7-124">EXAMPLES</span></span>

### <span data-ttu-id="c46f7-125">範例 1</span><span class="sxs-lookup"><span data-stu-id="c46f7-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="c46f7-126">在此範例中，變更偵測是在同步處理 Azure 檔案共用之「資料」和「Reporting\Templates」目錄中執行。</span><span class="sxs-lookup"><span data-stu-id="c46f7-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="c46f7-127">所有路徑都相對於 Azure 檔案共用命名空間的根目錄。</span><span class="sxs-lookup"><span data-stu-id="c46f7-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="c46f7-128">範例 2</span><span class="sxs-lookup"><span data-stu-id="c46f7-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="c46f7-129">在此範例中，變更偵測會針對一組命令來電者已知已變更的檔案執行。</span><span class="sxs-lookup"><span data-stu-id="c46f7-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="c46f7-130">目標是讓 Azure 檔案同步同步偵測及同步這些變更。</span><span class="sxs-lookup"><span data-stu-id="c46f7-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="c46f7-131">範例 3</span><span class="sxs-lookup"><span data-stu-id="c46f7-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="c46f7-132">在此範例中，變更偵測會針對「範例」目錄執行，並且會以遞迴性偵測子目錄中的變更。</span><span class="sxs-lookup"><span data-stu-id="c46f7-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="c46f7-133">請記住，如果路徑包含超過 10，000 個專案，Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c46f7-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="c46f7-134">如果路徑包含超過 10，000 個專案，請于命名空間的子部分上執行命令。</span><span class="sxs-lookup"><span data-stu-id="c46f7-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="c46f7-135">參數</span><span class="sxs-lookup"><span data-stu-id="c46f7-135">PARAMETERS</span></span>

### <span data-ttu-id="c46f7-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c46f7-136">-AsJob</span></span>
<span data-ttu-id="c46f7-137">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c46f7-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c46f7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46f7-138">-DefaultProfile</span></span>
<span data-ttu-id="c46f7-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c46f7-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c46f7-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="c46f7-140">-DirectoryPath</span></span>
<span data-ttu-id="c46f7-141">會執行變更偵測的目錄。</span><span class="sxs-lookup"><span data-stu-id="c46f7-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="c46f7-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c46f7-142">-InputObject</span></span>
<span data-ttu-id="c46f7-143">CloudEndpoint 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="c46f7-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c46f7-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="c46f7-144">-Name</span></span>
<span data-ttu-id="c46f7-145">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c46f7-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="c46f7-146">名稱是 GUID，而不是入口網站中顯示的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="c46f7-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="c46f7-147">若要取得 CloudEndpointName，請使用 Get-AzStorageSyncCloudEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c46f7-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="c46f7-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c46f7-148">-PassThru</span></span>
<span data-ttu-id="c46f7-149">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="c46f7-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c46f7-150">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="c46f7-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c46f7-151">-路徑</span><span class="sxs-lookup"><span data-stu-id="c46f7-151">-Path</span></span>
<span data-ttu-id="c46f7-152">執行變更偵測的路徑。</span><span class="sxs-lookup"><span data-stu-id="c46f7-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="c46f7-153">-遞迴</span><span class="sxs-lookup"><span data-stu-id="c46f7-153">-Recursive</span></span>
<span data-ttu-id="c46f7-154">指示目錄變更偵測是否為遞迴。</span><span class="sxs-lookup"><span data-stu-id="c46f7-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="c46f7-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46f7-155">-ResourceGroupName</span></span>
<span data-ttu-id="c46f7-156">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c46f7-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="c46f7-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c46f7-157">-ResourceId</span></span>
<span data-ttu-id="c46f7-158">CloudEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c46f7-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="c46f7-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c46f7-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="c46f7-160">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c46f7-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c46f7-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c46f7-161">-SyncGroupName</span></span>
<span data-ttu-id="c46f7-162">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c46f7-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c46f7-163">-確認</span><span class="sxs-lookup"><span data-stu-id="c46f7-163">-Confirm</span></span>
<span data-ttu-id="c46f7-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c46f7-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c46f7-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46f7-165">-WhatIf</span></span>
<span data-ttu-id="c46f7-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c46f7-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c46f7-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c46f7-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c46f7-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46f7-168">CommonParameters</span></span>
<span data-ttu-id="c46f7-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c46f7-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46f7-170">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c46f7-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46f7-171">輸入</span><span class="sxs-lookup"><span data-stu-id="c46f7-171">INPUTS</span></span>

### <span data-ttu-id="c46f7-172">System.String</span><span class="sxs-lookup"><span data-stu-id="c46f7-172">System.String</span></span>

### <span data-ttu-id="c46f7-173">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c46f7-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="c46f7-174">輸出</span><span class="sxs-lookup"><span data-stu-id="c46f7-174">OUTPUTS</span></span>

### <span data-ttu-id="c46f7-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="c46f7-175">System.Void</span></span>

## <span data-ttu-id="c46f7-176">筆記</span><span class="sxs-lookup"><span data-stu-id="c46f7-176">NOTES</span></span>

## <span data-ttu-id="c46f7-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="c46f7-177">RELATED LINKS</span></span>
