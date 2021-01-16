---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283327"
---
# <span data-ttu-id="555e9-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="555e9-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="555e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="555e9-102">SYNOPSIS</span></span>
<span data-ttu-id="555e9-103">這個命令會從同步處理群組中刪除指定的雲端端點。</span><span class="sxs-lookup"><span data-stu-id="555e9-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="555e9-104">若沒有至少一個雲端端點，此同步處理群組中則不能同步處理任何其他伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="555e9-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="555e9-105">句法</span><span class="sxs-lookup"><span data-stu-id="555e9-105">SYNTAX</span></span>

### <span data-ttu-id="555e9-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="555e9-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="555e9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="555e9-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="555e9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="555e9-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="555e9-109">說明</span><span class="sxs-lookup"><span data-stu-id="555e9-109">DESCRIPTION</span></span>
<span data-ttu-id="555e9-110">這個命令會從同步處理群組中刪除指定的雲端端點。</span><span class="sxs-lookup"><span data-stu-id="555e9-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="555e9-111">Azure 檔案共用雲端端點參照在此程式中保持不變。</span><span class="sxs-lookup"><span data-stu-id="555e9-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="555e9-112">此命令僅供解除授權時用。</span><span class="sxs-lookup"><span data-stu-id="555e9-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="555e9-113">移除雲端端點是破壞性的操作。</span><span class="sxs-lookup"><span data-stu-id="555e9-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="555e9-114">如果沒有至少一個雲端端點存在，伺服器端點就無法進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="555e9-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="555e9-115">不應該執行此作業來解決同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="555e9-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="555e9-116">如果此 Azure 檔案共用再次新增至同一個同步處理群組（作為雲端端點），可能會導致衝突檔案和其他不預期的結果。</span><span class="sxs-lookup"><span data-stu-id="555e9-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="555e9-117">示例</span><span class="sxs-lookup"><span data-stu-id="555e9-117">EXAMPLES</span></span>

### <span data-ttu-id="555e9-118">範例1</span><span class="sxs-lookup"><span data-stu-id="555e9-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="555e9-119">這個命令會移除雲端端點。</span><span class="sxs-lookup"><span data-stu-id="555e9-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="555e9-120">參數</span><span class="sxs-lookup"><span data-stu-id="555e9-120">PARAMETERS</span></span>

### <span data-ttu-id="555e9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="555e9-121">-AsJob</span></span>
<span data-ttu-id="555e9-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="555e9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="555e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555e9-123">-DefaultProfile</span></span>
<span data-ttu-id="555e9-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="555e9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="555e9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="555e9-125">-Force</span></span>
<span data-ttu-id="555e9-126">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="555e9-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="555e9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="555e9-127">-InputObject</span></span>
<span data-ttu-id="555e9-128">CloudEndpoint 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="555e9-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="555e9-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="555e9-129">-Name</span></span>
<span data-ttu-id="555e9-130">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="555e9-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="555e9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="555e9-131">-PassThru</span></span>
<span data-ttu-id="555e9-132">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="555e9-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="555e9-133">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="555e9-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="555e9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555e9-134">-ResourceGroupName</span></span>
<span data-ttu-id="555e9-135">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="555e9-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="555e9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="555e9-136">-ResourceId</span></span>
<span data-ttu-id="555e9-137">CloudEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="555e9-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="555e9-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="555e9-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="555e9-139">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="555e9-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="555e9-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="555e9-140">-SyncGroupName</span></span>
<span data-ttu-id="555e9-141">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="555e9-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="555e9-142">-確認</span><span class="sxs-lookup"><span data-stu-id="555e9-142">-Confirm</span></span>
<span data-ttu-id="555e9-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="555e9-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="555e9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="555e9-144">-WhatIf</span></span>
<span data-ttu-id="555e9-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="555e9-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="555e9-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="555e9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="555e9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555e9-147">CommonParameters</span></span>
<span data-ttu-id="555e9-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="555e9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555e9-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="555e9-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555e9-150">輸入</span><span class="sxs-lookup"><span data-stu-id="555e9-150">INPUTS</span></span>

### <span data-ttu-id="555e9-151">PSCloudEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="555e9-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="555e9-152">System.object</span><span class="sxs-lookup"><span data-stu-id="555e9-152">System.String</span></span>

## <span data-ttu-id="555e9-153">輸出</span><span class="sxs-lookup"><span data-stu-id="555e9-153">OUTPUTS</span></span>

### <span data-ttu-id="555e9-154">System.object</span><span class="sxs-lookup"><span data-stu-id="555e9-154">System.Object</span></span>
## <span data-ttu-id="555e9-155">筆記</span><span class="sxs-lookup"><span data-stu-id="555e9-155">NOTES</span></span>

## <span data-ttu-id="555e9-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="555e9-156">RELATED LINKS</span></span>
