---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 06eb3942a5320ff7c5c8bb3d089ecad2da912edb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793177"
---
# <span data-ttu-id="4f31b-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="4f31b-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="4f31b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f31b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f31b-103">這個命令會將所有的分層檔案撤回回本機磁片。</span><span class="sxs-lookup"><span data-stu-id="4f31b-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="4f31b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f31b-104">SYNTAX</span></span>

### <span data-ttu-id="4f31b-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4f31b-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f31b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f31b-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f31b-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f31b-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f31b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4f31b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f31b-109">在伺服器端點上啟用雲端分層之後 (在已登錄伺服器上的特定位置) ，就可以使用此命令，將所有的分層檔案撤回到本機磁片。</span><span class="sxs-lookup"><span data-stu-id="4f31b-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="4f31b-110">強烈建議您先在此伺服器端點上停用雲端堆疊，然後再開始撤回。</span><span class="sxs-lookup"><span data-stu-id="4f31b-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="4f31b-111">如果堆疊仍開啟，則召回可能會導致其他檔案在進行分級，以達到在本機磁片上的所有內容所需的目標。</span><span class="sxs-lookup"><span data-stu-id="4f31b-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="4f31b-112">示例</span><span class="sxs-lookup"><span data-stu-id="4f31b-112">EXAMPLES</span></span>

### <span data-ttu-id="4f31b-113">範例1</span><span class="sxs-lookup"><span data-stu-id="4f31b-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="4f31b-114">這個命令會以遞迴方式，撤回位於指定伺服器端點之根路徑下的所有分層檔案。</span><span class="sxs-lookup"><span data-stu-id="4f31b-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="4f31b-115">參數</span><span class="sxs-lookup"><span data-stu-id="4f31b-115">PARAMETERS</span></span>

### <span data-ttu-id="4f31b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f31b-116">-AsJob</span></span>
<span data-ttu-id="4f31b-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f31b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f31b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f31b-118">-DefaultProfile</span></span>
<span data-ttu-id="4f31b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f31b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f31b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f31b-120">-InputObject</span></span>
<span data-ttu-id="4f31b-121">SyncGroup 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="4f31b-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f31b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f31b-122">-Name</span></span>
<span data-ttu-id="4f31b-123">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f31b-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f31b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f31b-124">-PassThru</span></span>
<span data-ttu-id="4f31b-125">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f31b-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4f31b-126">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="4f31b-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4f31b-127">-模式</span><span class="sxs-lookup"><span data-stu-id="4f31b-127">-Pattern</span></span>
<span data-ttu-id="4f31b-128">檔案名的模式</span><span class="sxs-lookup"><span data-stu-id="4f31b-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="4f31b-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="4f31b-129">-RecallPath</span></span>
<span data-ttu-id="4f31b-130">召回需要召回的路徑。</span><span class="sxs-lookup"><span data-stu-id="4f31b-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="4f31b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f31b-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f31b-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4f31b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="4f31b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f31b-133">-ResourceId</span></span>
<span data-ttu-id="4f31b-134">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4f31b-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4f31b-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4f31b-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="4f31b-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f31b-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4f31b-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4f31b-137">-SyncGroupName</span></span>
<span data-ttu-id="4f31b-138">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f31b-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4f31b-139">-確認</span><span class="sxs-lookup"><span data-stu-id="4f31b-139">-Confirm</span></span>
<span data-ttu-id="4f31b-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f31b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f31b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f31b-141">-WhatIf</span></span>
<span data-ttu-id="4f31b-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f31b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f31b-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f31b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f31b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f31b-144">CommonParameters</span></span>
<span data-ttu-id="4f31b-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f31b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f31b-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f31b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f31b-147">輸入</span><span class="sxs-lookup"><span data-stu-id="4f31b-147">INPUTS</span></span>

### <span data-ttu-id="4f31b-148">System.object</span><span class="sxs-lookup"><span data-stu-id="4f31b-148">System.String</span></span>

### <span data-ttu-id="4f31b-149">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="4f31b-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4f31b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="4f31b-150">OUTPUTS</span></span>

### <span data-ttu-id="4f31b-151">System.object</span><span class="sxs-lookup"><span data-stu-id="4f31b-151">System.Boolean</span></span>

## <span data-ttu-id="4f31b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="4f31b-152">NOTES</span></span>

## <span data-ttu-id="4f31b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f31b-153">RELATED LINKS</span></span>
