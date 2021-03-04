---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 451df6b0608ece9888b1525388784dcee1aac334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907441"
---
# <span data-ttu-id="082ba-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="082ba-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="082ba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="082ba-102">SYNOPSIS</span></span>
<span data-ttu-id="082ba-103">此命令會從同步處理群組中刪除指定的雲端端點。</span><span class="sxs-lookup"><span data-stu-id="082ba-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="082ba-104">沒有至少一個雲端端點，此同步處理群組中沒有任何其他伺服器端點可以同步處理。</span><span class="sxs-lookup"><span data-stu-id="082ba-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="082ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="082ba-105">SYNTAX</span></span>

### <span data-ttu-id="082ba-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="082ba-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="082ba-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="082ba-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="082ba-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="082ba-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="082ba-109">描述</span><span class="sxs-lookup"><span data-stu-id="082ba-109">DESCRIPTION</span></span>
<span data-ttu-id="082ba-110">此命令會從同步處理群組中刪除指定的雲端端點。</span><span class="sxs-lookup"><span data-stu-id="082ba-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="082ba-111">共用雲端端點參照的 Azure 檔案會不受此程式觸控。</span><span class="sxs-lookup"><span data-stu-id="082ba-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="082ba-112">此命令僅適用于解除授權。</span><span class="sxs-lookup"><span data-stu-id="082ba-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="082ba-113">移除雲端端點是一項破壞性的作業。</span><span class="sxs-lookup"><span data-stu-id="082ba-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="082ba-114">伺服器端點必須至少有一個雲端端點，就無法同步處理。</span><span class="sxs-lookup"><span data-stu-id="082ba-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="082ba-115">此作業不應執行以解決同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="082ba-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="082ba-116">如果這個 Azure 檔案共用再次新增到與雲端端點相同的同步處理群組，可能會導致衝突檔案和其他非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="082ba-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="082ba-117">例子</span><span class="sxs-lookup"><span data-stu-id="082ba-117">EXAMPLES</span></span>

### <span data-ttu-id="082ba-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="082ba-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="082ba-119">此命令會移除雲端端點。</span><span class="sxs-lookup"><span data-stu-id="082ba-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="082ba-120">參數</span><span class="sxs-lookup"><span data-stu-id="082ba-120">PARAMETERS</span></span>

### <span data-ttu-id="082ba-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="082ba-121">-AsJob</span></span>
<span data-ttu-id="082ba-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="082ba-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="082ba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082ba-123">-DefaultProfile</span></span>
<span data-ttu-id="082ba-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="082ba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="082ba-125">-強制</span><span class="sxs-lookup"><span data-stu-id="082ba-125">-Force</span></span>
<span data-ttu-id="082ba-126">提供 -強制跳過此命令的確認。</span><span class="sxs-lookup"><span data-stu-id="082ba-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="082ba-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="082ba-127">-InputObject</span></span>
<span data-ttu-id="082ba-128">CloudEndpoint 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="082ba-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="082ba-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="082ba-129">-Name</span></span>
<span data-ttu-id="082ba-130">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="082ba-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082ba-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="082ba-131">-PassThru</span></span>
<span data-ttu-id="082ba-132">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="082ba-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="082ba-133">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="082ba-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="082ba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082ba-134">-ResourceGroupName</span></span>
<span data-ttu-id="082ba-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="082ba-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="082ba-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="082ba-136">-ResourceId</span></span>
<span data-ttu-id="082ba-137">CloudEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="082ba-137">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="082ba-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="082ba-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="082ba-139">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="082ba-139">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082ba-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="082ba-140">-SyncGroupName</span></span>
<span data-ttu-id="082ba-141">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="082ba-141">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082ba-142">-確認</span><span class="sxs-lookup"><span data-stu-id="082ba-142">-Confirm</span></span>
<span data-ttu-id="082ba-143">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="082ba-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082ba-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082ba-144">-WhatIf</span></span>
<span data-ttu-id="082ba-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="082ba-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="082ba-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="082ba-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082ba-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082ba-147">CommonParameters</span></span>
<span data-ttu-id="082ba-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="082ba-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082ba-149">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="082ba-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082ba-150">輸入</span><span class="sxs-lookup"><span data-stu-id="082ba-150">INPUTS</span></span>

### <span data-ttu-id="082ba-151">Microsoft.Azure.Commands.StorageSync.models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="082ba-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="082ba-152">System.String</span><span class="sxs-lookup"><span data-stu-id="082ba-152">System.String</span></span>

## <span data-ttu-id="082ba-153">輸出</span><span class="sxs-lookup"><span data-stu-id="082ba-153">OUTPUTS</span></span>

### <span data-ttu-id="082ba-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="082ba-154">System.Object</span></span>
## <span data-ttu-id="082ba-155">筆記</span><span class="sxs-lookup"><span data-stu-id="082ba-155">NOTES</span></span>

## <span data-ttu-id="082ba-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="082ba-156">RELATED LINKS</span></span>
