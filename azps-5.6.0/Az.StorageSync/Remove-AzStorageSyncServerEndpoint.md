---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: ed0f21c7a3ad2105073cb81a8dff174d201f96ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907429"
---
# <span data-ttu-id="ed09e-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed09e-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ed09e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed09e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed09e-103">此命令將會刪除指定的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="ed09e-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="ed09e-104">同步處理到這個位置將會立即停止。</span><span class="sxs-lookup"><span data-stu-id="ed09e-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="ed09e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed09e-105">SYNTAX</span></span>

### <span data-ttu-id="ed09e-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ed09e-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed09e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed09e-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed09e-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed09e-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed09e-109">描述</span><span class="sxs-lookup"><span data-stu-id="ed09e-109">DESCRIPTION</span></span>
<span data-ttu-id="ed09e-110">移除伺服器端點是一項破壞性的作業。</span><span class="sxs-lookup"><span data-stu-id="ed09e-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="ed09e-111">此伺服器位置將會停止同步處理。</span><span class="sxs-lookup"><span data-stu-id="ed09e-111">This server location will stop syncing.</span></span> <span data-ttu-id="ed09e-112">此作業不應執行以解決同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="ed09e-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="ed09e-113">如果這個伺服器 (包括：檔案) 會再次新增到與伺服器端點相同的同步處理群組中，可能會導致衝突檔案和其他非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="ed09e-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="ed09e-114">此命令僅適用于解除授權。</span><span class="sxs-lookup"><span data-stu-id="ed09e-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="ed09e-115">例子</span><span class="sxs-lookup"><span data-stu-id="ed09e-115">EXAMPLES</span></span>

### <span data-ttu-id="ed09e-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="ed09e-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="ed09e-117">此命令會移除伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="ed09e-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="ed09e-118">參數</span><span class="sxs-lookup"><span data-stu-id="ed09e-118">PARAMETERS</span></span>

### <span data-ttu-id="ed09e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed09e-119">-AsJob</span></span>
<span data-ttu-id="ed09e-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ed09e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed09e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed09e-121">-DefaultProfile</span></span>
<span data-ttu-id="ed09e-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed09e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed09e-123">-強制</span><span class="sxs-lookup"><span data-stu-id="ed09e-123">-Force</span></span>
<span data-ttu-id="ed09e-124">提供 -強制跳過此命令的確認。</span><span class="sxs-lookup"><span data-stu-id="ed09e-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="ed09e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed09e-125">-InputObject</span></span>
<span data-ttu-id="ed09e-126">ServerEndpoint 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="ed09e-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed09e-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed09e-127">-Name</span></span>
<span data-ttu-id="ed09e-128">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed09e-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="ed09e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed09e-129">-PassThru</span></span>
<span data-ttu-id="ed09e-130">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="ed09e-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="ed09e-131">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="ed09e-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="ed09e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed09e-132">-ResourceGroupName</span></span>
<span data-ttu-id="ed09e-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ed09e-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed09e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed09e-134">-ResourceId</span></span>
<span data-ttu-id="ed09e-135">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ed09e-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ed09e-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ed09e-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="ed09e-137">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed09e-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ed09e-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ed09e-138">-SyncGroupName</span></span>
<span data-ttu-id="ed09e-139">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed09e-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ed09e-140">-確認</span><span class="sxs-lookup"><span data-stu-id="ed09e-140">-Confirm</span></span>
<span data-ttu-id="ed09e-141">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ed09e-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed09e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed09e-142">-WhatIf</span></span>
<span data-ttu-id="ed09e-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed09e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed09e-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed09e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed09e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed09e-145">CommonParameters</span></span>
<span data-ttu-id="ed09e-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed09e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed09e-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ed09e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed09e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="ed09e-148">INPUTS</span></span>

### <span data-ttu-id="ed09e-149">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed09e-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="ed09e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ed09e-150">System.String</span></span>

## <span data-ttu-id="ed09e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="ed09e-151">OUTPUTS</span></span>

### <span data-ttu-id="ed09e-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="ed09e-152">System.Object</span></span>
## <span data-ttu-id="ed09e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="ed09e-153">NOTES</span></span>

## <span data-ttu-id="ed09e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed09e-154">RELATED LINKS</span></span>
