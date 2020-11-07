---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793179"
---
# <span data-ttu-id="509b3-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="509b3-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="509b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="509b3-102">SYNOPSIS</span></span>
<span data-ttu-id="509b3-103">這個命令可以用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="509b3-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="509b3-104">您可以將它設定為整個共用、子資料夾或一組檔案的目標。</span><span class="sxs-lookup"><span data-stu-id="509b3-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="509b3-105">最多可以檢測到10000變更。</span><span class="sxs-lookup"><span data-stu-id="509b3-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="509b3-106">如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。</span><span class="sxs-lookup"><span data-stu-id="509b3-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="509b3-107">句法</span><span class="sxs-lookup"><span data-stu-id="509b3-107">SYNTAX</span></span>

### <span data-ttu-id="509b3-108">StringAndDirectoryParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="509b3-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509b3-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="509b3-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509b3-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="509b3-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509b3-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="509b3-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509b3-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="509b3-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509b3-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="509b3-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="509b3-114">說明</span><span class="sxs-lookup"><span data-stu-id="509b3-114">DESCRIPTION</span></span>
<span data-ttu-id="509b3-115">Azure 檔案同步處理會定期檢查同步處理 Azure 檔案共用中的命名空間，以取得與同步處理之外的其他方法所帶來的變更。目標是識別這些變更，並最終將它們同步處理到已連線的伺服器。</span><span class="sxs-lookup"><span data-stu-id="509b3-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="509b3-116">這個命令可以用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="509b3-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="509b3-117">您可以將它設定為整個共用、子資料夾或一組檔案的目標。</span><span class="sxs-lookup"><span data-stu-id="509b3-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="509b3-118">如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。</span><span class="sxs-lookup"><span data-stu-id="509b3-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="509b3-119">示例</span><span class="sxs-lookup"><span data-stu-id="509b3-119">EXAMPLES</span></span>

### <span data-ttu-id="509b3-120">範例1</span><span class="sxs-lookup"><span data-stu-id="509b3-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="509b3-121">在這個範例中，變更偵測會在同步處理 Azure 檔案共用的「資料」和「Reporting\Templates」目錄中執行。</span><span class="sxs-lookup"><span data-stu-id="509b3-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="509b3-122">所有路徑都是相對於 Azure 檔案共用命名空間的根。</span><span class="sxs-lookup"><span data-stu-id="509b3-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="509b3-123">範例2</span><span class="sxs-lookup"><span data-stu-id="509b3-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="509b3-124">在這個範例中，針對命令呼叫者已知已變更的一組檔案，會執行變更偵測。</span><span class="sxs-lookup"><span data-stu-id="509b3-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="509b3-125">我們的目標是讓 Azure 檔案同步偵測並同步處理這些變更。</span><span class="sxs-lookup"><span data-stu-id="509b3-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="509b3-126">範例3</span><span class="sxs-lookup"><span data-stu-id="509b3-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="509b3-127">在這個範例中，會針對「範例」目錄執行變更偵測，並以遞迴方式檢測子目錄中的變更。</span><span class="sxs-lookup"><span data-stu-id="509b3-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="509b3-128">請記住，此命令可以在自動中止前檢測到10000變更。</span><span class="sxs-lookup"><span data-stu-id="509b3-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="509b3-129">如果您懷疑已發生10000以上的變更，請在命名空間的子元件上執行命令。</span><span class="sxs-lookup"><span data-stu-id="509b3-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="509b3-130">參數</span><span class="sxs-lookup"><span data-stu-id="509b3-130">PARAMETERS</span></span>

### <span data-ttu-id="509b3-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="509b3-131">-AsJob</span></span>
<span data-ttu-id="509b3-132">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="509b3-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="509b3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509b3-133">-DefaultProfile</span></span>
<span data-ttu-id="509b3-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="509b3-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="509b3-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="509b3-135">-DirectoryPath</span></span>
<span data-ttu-id="509b3-136">將執行變更偵測的目錄。</span><span class="sxs-lookup"><span data-stu-id="509b3-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="509b3-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="509b3-137">-InputObject</span></span>
<span data-ttu-id="509b3-138">CloudEndpoint 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="509b3-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="509b3-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="509b3-139">-Name</span></span>
<span data-ttu-id="509b3-140">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="509b3-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="509b3-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="509b3-141">-PassThru</span></span>
<span data-ttu-id="509b3-142">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="509b3-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="509b3-143">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="509b3-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="509b3-144">-Path</span><span class="sxs-lookup"><span data-stu-id="509b3-144">-Path</span></span>
<span data-ttu-id="509b3-145">將執行變更偵測的路徑。</span><span class="sxs-lookup"><span data-stu-id="509b3-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="509b3-146">-Recursive</span><span class="sxs-lookup"><span data-stu-id="509b3-146">-Recursive</span></span>
<span data-ttu-id="509b3-147">指示目錄變更檢測是否為遞迴式。</span><span class="sxs-lookup"><span data-stu-id="509b3-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="509b3-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="509b3-148">-ResourceGroupName</span></span>
<span data-ttu-id="509b3-149">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="509b3-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="509b3-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="509b3-150">-ResourceId</span></span>
<span data-ttu-id="509b3-151">CloudEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="509b3-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="509b3-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="509b3-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="509b3-153">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="509b3-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="509b3-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="509b3-154">-SyncGroupName</span></span>
<span data-ttu-id="509b3-155">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="509b3-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="509b3-156">-確認</span><span class="sxs-lookup"><span data-stu-id="509b3-156">-Confirm</span></span>
<span data-ttu-id="509b3-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="509b3-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="509b3-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="509b3-158">-WhatIf</span></span>
<span data-ttu-id="509b3-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="509b3-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="509b3-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="509b3-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="509b3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509b3-161">CommonParameters</span></span>
<span data-ttu-id="509b3-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="509b3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509b3-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="509b3-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509b3-164">輸入</span><span class="sxs-lookup"><span data-stu-id="509b3-164">INPUTS</span></span>

### <span data-ttu-id="509b3-165">System.object</span><span class="sxs-lookup"><span data-stu-id="509b3-165">System.String</span></span>

### <span data-ttu-id="509b3-166">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="509b3-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="509b3-167">輸出</span><span class="sxs-lookup"><span data-stu-id="509b3-167">OUTPUTS</span></span>

### <span data-ttu-id="509b3-168">System.void</span><span class="sxs-lookup"><span data-stu-id="509b3-168">System.Void</span></span>

## <span data-ttu-id="509b3-169">筆記</span><span class="sxs-lookup"><span data-stu-id="509b3-169">NOTES</span></span>

## <span data-ttu-id="509b3-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="509b3-170">RELATED LINKS</span></span>
