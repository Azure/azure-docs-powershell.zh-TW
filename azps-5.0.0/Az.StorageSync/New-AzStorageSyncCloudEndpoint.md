---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287652"
---
# <span data-ttu-id="059b7-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="059b7-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="059b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="059b7-102">SYNOPSIS</span></span>
<span data-ttu-id="059b7-103">這個命令會在同步處理群組中建立 Azure 檔案同步處理雲端端點。</span><span class="sxs-lookup"><span data-stu-id="059b7-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="059b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="059b7-104">SYNTAX</span></span>

### <span data-ttu-id="059b7-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="059b7-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="059b7-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="059b7-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059b7-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="059b7-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059b7-108">說明</span><span class="sxs-lookup"><span data-stu-id="059b7-108">DESCRIPTION</span></span>
<span data-ttu-id="059b7-109">這個命令會建立 Azure 檔案同步處理雲端端點。</span><span class="sxs-lookup"><span data-stu-id="059b7-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="059b7-110">雲端端點是對現有 Azure 檔案共用的參照。</span><span class="sxs-lookup"><span data-stu-id="059b7-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="059b7-111">它代表檔案共用，並定義 it 參與同步處理已在其中建立雲端端點之同步群組的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="059b7-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="059b7-112">示例</span><span class="sxs-lookup"><span data-stu-id="059b7-112">EXAMPLES</span></span>

### <span data-ttu-id="059b7-113">範例1</span><span class="sxs-lookup"><span data-stu-id="059b7-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="059b7-114">雲端端點是同步群組的一個有機成員，這是在名為「mySyncGroupName」的現有同步處理群組內建立一個範例。</span><span class="sxs-lookup"><span data-stu-id="059b7-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="059b7-115">參數</span><span class="sxs-lookup"><span data-stu-id="059b7-115">PARAMETERS</span></span>

### <span data-ttu-id="059b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="059b7-116">-AsJob</span></span>
<span data-ttu-id="059b7-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="059b7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="059b7-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="059b7-118">-AzureFileShareName</span></span>
<span data-ttu-id="059b7-119">儲存空間帳戶共用名稱稱 (Azure 檔案共用名稱稱) </span><span class="sxs-lookup"><span data-stu-id="059b7-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="059b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059b7-120">-DefaultProfile</span></span>
<span data-ttu-id="059b7-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="059b7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059b7-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="059b7-122">-Name</span></span>
<span data-ttu-id="059b7-123">雲端端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="059b7-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="059b7-124">透過 Azure 入口網站建立時，名稱會設定為它所參照之 Azure 檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="059b7-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="059b7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="059b7-125">-ParentObject</span></span>
<span data-ttu-id="059b7-126">SyncGroup 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="059b7-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="059b7-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="059b7-127">-ParentResourceId</span></span>
<span data-ttu-id="059b7-128">SyncGroup 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="059b7-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="059b7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059b7-129">-ResourceGroupName</span></span>
<span data-ttu-id="059b7-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="059b7-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="059b7-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="059b7-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="059b7-132">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="059b7-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="059b7-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="059b7-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="059b7-134">儲存帳戶租使用者識別碼 (公司目錄識別碼) </span><span class="sxs-lookup"><span data-stu-id="059b7-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="059b7-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="059b7-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="059b7-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="059b7-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="059b7-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="059b7-137">-SyncGroupName</span></span>
<span data-ttu-id="059b7-138">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="059b7-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="059b7-139">-確認</span><span class="sxs-lookup"><span data-stu-id="059b7-139">-Confirm</span></span>
<span data-ttu-id="059b7-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="059b7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059b7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059b7-141">-WhatIf</span></span>
<span data-ttu-id="059b7-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="059b7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059b7-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="059b7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059b7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059b7-144">CommonParameters</span></span>
<span data-ttu-id="059b7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="059b7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059b7-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="059b7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059b7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="059b7-147">INPUTS</span></span>

### <span data-ttu-id="059b7-148">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="059b7-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="059b7-149">System.object</span><span class="sxs-lookup"><span data-stu-id="059b7-149">System.String</span></span>

## <span data-ttu-id="059b7-150">輸出</span><span class="sxs-lookup"><span data-stu-id="059b7-150">OUTPUTS</span></span>

### <span data-ttu-id="059b7-151">PSCloudEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="059b7-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="059b7-152">筆記</span><span class="sxs-lookup"><span data-stu-id="059b7-152">NOTES</span></span>

## <span data-ttu-id="059b7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="059b7-153">RELATED LINKS</span></span>
