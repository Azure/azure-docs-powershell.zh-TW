---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c55b49052ae34eba9dfff960c85e9ade7617d2a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916853"
---
# <span data-ttu-id="3c2ac-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c2ac-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="3c2ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2ac-103">此命令在同步處理群組中建立 Azure 檔案同步處理雲端端點。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="3c2ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c2ac-104">SYNTAX</span></span>

### <span data-ttu-id="3c2ac-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3c2ac-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2ac-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c2ac-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c2ac-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c2ac-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c2ac-108">描述</span><span class="sxs-lookup"><span data-stu-id="3c2ac-108">DESCRIPTION</span></span>
<span data-ttu-id="3c2ac-109">此命令會建立 Azure 檔案同步處理雲端端點。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="3c2ac-110">雲端端點是現有 Azure 檔案共用參照。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="3c2ac-111">它代表檔案共用，並定義它參與同步處理雲端端點已建立之同步處理群組的所有檔案部分。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="3c2ac-112">例子</span><span class="sxs-lookup"><span data-stu-id="3c2ac-112">EXAMPLES</span></span>

### <span data-ttu-id="3c2ac-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="3c2ac-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="3c2ac-114">雲端端點是同步處理群組中不可或缺的成員，這是在名為「mySyncGroupName」的現有同步處理群組內建立一個同步處理群組的範例。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="3c2ac-115">參數</span><span class="sxs-lookup"><span data-stu-id="3c2ac-115">PARAMETERS</span></span>

### <span data-ttu-id="3c2ac-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c2ac-116">-AsJob</span></span>
<span data-ttu-id="3c2ac-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c2ac-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c2ac-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="3c2ac-118">-AzureFileShareName</span></span>
<span data-ttu-id="3c2ac-119">儲存帳戶共用名稱稱 (Azure 檔案共用名稱稱) </span><span class="sxs-lookup"><span data-stu-id="3c2ac-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2ac-120">-DefaultProfile</span></span>
<span data-ttu-id="3c2ac-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c2ac-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c2ac-122">-Name</span></span>
<span data-ttu-id="3c2ac-123">雲端端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="3c2ac-124">透過 Azure 入口網站建立時，名稱會設定為 Azure 檔案共用參照的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3c2ac-125">-ParentObject</span></span>
<span data-ttu-id="3c2ac-126">SyncGroup 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3c2ac-127">-ParentResourceId</span></span>
<span data-ttu-id="3c2ac-128">SyncGroup 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3c2ac-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c2ac-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c2ac-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3c2ac-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="3c2ac-132">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3c2ac-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="3c2ac-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="3c2ac-134">儲存帳戶租使用者識別碼 (目錄識別碼) </span><span class="sxs-lookup"><span data-stu-id="3c2ac-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="3c2ac-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3c2ac-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="3c2ac-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3c2ac-137">-SyncGroupName</span></span>
<span data-ttu-id="3c2ac-138">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2ac-139">-確認</span><span class="sxs-lookup"><span data-stu-id="3c2ac-139">-Confirm</span></span>
<span data-ttu-id="3c2ac-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2ac-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2ac-141">-WhatIf</span></span>
<span data-ttu-id="3c2ac-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c2ac-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c2ac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2ac-144">CommonParameters</span></span>
<span data-ttu-id="3c2ac-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2ac-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3c2ac-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2ac-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3c2ac-147">INPUTS</span></span>

### <span data-ttu-id="3c2ac-148">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3c2ac-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="3c2ac-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3c2ac-149">System.String</span></span>

## <span data-ttu-id="3c2ac-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3c2ac-150">OUTPUTS</span></span>

### <span data-ttu-id="3c2ac-151">Microsoft.Azure.Commands.StorageSync.models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c2ac-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="3c2ac-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3c2ac-152">NOTES</span></span>

## <span data-ttu-id="3c2ac-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c2ac-153">RELATED LINKS</span></span>
