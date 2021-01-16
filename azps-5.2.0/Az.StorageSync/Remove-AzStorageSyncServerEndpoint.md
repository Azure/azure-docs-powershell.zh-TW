---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283319"
---
# <span data-ttu-id="8fb66-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fb66-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="8fb66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fb66-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb66-103">這個命令會刪除指定的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="8fb66-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="8fb66-104">同步處理到這個位置將會立即停止。</span><span class="sxs-lookup"><span data-stu-id="8fb66-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="8fb66-105">句法</span><span class="sxs-lookup"><span data-stu-id="8fb66-105">SYNTAX</span></span>

### <span data-ttu-id="8fb66-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8fb66-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fb66-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb66-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fb66-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb66-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fb66-109">說明</span><span class="sxs-lookup"><span data-stu-id="8fb66-109">DESCRIPTION</span></span>
<span data-ttu-id="8fb66-110">移除伺服器端點是破壞性操作。</span><span class="sxs-lookup"><span data-stu-id="8fb66-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="8fb66-111">這個伺服器位置將會停止同步處理。</span><span class="sxs-lookup"><span data-stu-id="8fb66-111">This server location will stop syncing.</span></span> <span data-ttu-id="8fb66-112">不應該執行此作業來解決同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="8fb66-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="8fb66-113">如果此伺服器位置 (包括在內，) 會再次新增到與伺服器端點相同的同步處理群組中，這可能會導致衝突檔案和其他不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="8fb66-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="8fb66-114">這個命令僅供解除授權。</span><span class="sxs-lookup"><span data-stu-id="8fb66-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="8fb66-115">示例</span><span class="sxs-lookup"><span data-stu-id="8fb66-115">EXAMPLES</span></span>

### <span data-ttu-id="8fb66-116">範例1</span><span class="sxs-lookup"><span data-stu-id="8fb66-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="8fb66-117">這個命令會移除伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="8fb66-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="8fb66-118">參數</span><span class="sxs-lookup"><span data-stu-id="8fb66-118">PARAMETERS</span></span>

### <span data-ttu-id="8fb66-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fb66-119">-AsJob</span></span>
<span data-ttu-id="8fb66-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8fb66-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fb66-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb66-121">-DefaultProfile</span></span>
<span data-ttu-id="8fb66-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8fb66-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fb66-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8fb66-123">-Force</span></span>
<span data-ttu-id="8fb66-124">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="8fb66-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="8fb66-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fb66-125">-InputObject</span></span>
<span data-ttu-id="8fb66-126">ServerEndpoint 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="8fb66-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="8fb66-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fb66-127">-Name</span></span>
<span data-ttu-id="8fb66-128">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb66-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="8fb66-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fb66-129">-PassThru</span></span>
<span data-ttu-id="8fb66-130">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8fb66-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="8fb66-131">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="8fb66-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="8fb66-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb66-132">-ResourceGroupName</span></span>
<span data-ttu-id="8fb66-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb66-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="8fb66-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fb66-134">-ResourceId</span></span>
<span data-ttu-id="8fb66-135">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8fb66-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="8fb66-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="8fb66-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="8fb66-137">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb66-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8fb66-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb66-138">-SyncGroupName</span></span>
<span data-ttu-id="8fb66-139">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb66-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="8fb66-140">-確認</span><span class="sxs-lookup"><span data-stu-id="8fb66-140">-Confirm</span></span>
<span data-ttu-id="8fb66-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8fb66-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fb66-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fb66-142">-WhatIf</span></span>
<span data-ttu-id="8fb66-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8fb66-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fb66-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8fb66-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fb66-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb66-145">CommonParameters</span></span>
<span data-ttu-id="8fb66-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fb66-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb66-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fb66-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb66-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8fb66-148">INPUTS</span></span>

### <span data-ttu-id="8fb66-149">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="8fb66-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="8fb66-150">System.object</span><span class="sxs-lookup"><span data-stu-id="8fb66-150">System.String</span></span>

## <span data-ttu-id="8fb66-151">輸出</span><span class="sxs-lookup"><span data-stu-id="8fb66-151">OUTPUTS</span></span>

### <span data-ttu-id="8fb66-152">System.object</span><span class="sxs-lookup"><span data-stu-id="8fb66-152">System.Object</span></span>
## <span data-ttu-id="8fb66-153">筆記</span><span class="sxs-lookup"><span data-stu-id="8fb66-153">NOTES</span></span>

## <span data-ttu-id="8fb66-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fb66-154">RELATED LINKS</span></span>
