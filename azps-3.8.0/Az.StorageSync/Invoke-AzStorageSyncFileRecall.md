---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959072"
---
# <span data-ttu-id="aaeef-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="aaeef-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="aaeef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aaeef-102">SYNOPSIS</span></span>
<span data-ttu-id="aaeef-103">這個命令會將所有的分層檔案撤回回本機磁片。</span><span class="sxs-lookup"><span data-stu-id="aaeef-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="aaeef-104">句法</span><span class="sxs-lookup"><span data-stu-id="aaeef-104">SYNTAX</span></span>

### <span data-ttu-id="aaeef-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aaeef-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaeef-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaeef-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaeef-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaeef-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaeef-108">說明</span><span class="sxs-lookup"><span data-stu-id="aaeef-108">DESCRIPTION</span></span>
<span data-ttu-id="aaeef-109">在伺服器端點上啟用雲端分層之後 (在已登錄伺服器上的特定位置) ，就可以使用此命令，將所有的分層檔案撤回到本機磁片。</span><span class="sxs-lookup"><span data-stu-id="aaeef-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="aaeef-110">強烈建議您先在此伺服器端點上停用雲端堆疊，然後再開始撤回。</span><span class="sxs-lookup"><span data-stu-id="aaeef-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="aaeef-111">如果堆疊仍開啟，則召回可能會導致其他檔案在進行分級，以達到在本機磁片上的所有內容所需的目標。</span><span class="sxs-lookup"><span data-stu-id="aaeef-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="aaeef-112">示例</span><span class="sxs-lookup"><span data-stu-id="aaeef-112">EXAMPLES</span></span>

### <span data-ttu-id="aaeef-113">範例1</span><span class="sxs-lookup"><span data-stu-id="aaeef-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="aaeef-114">這個命令會以遞迴方式，撤回位於指定伺服器端點之根路徑下的所有分層檔案。</span><span class="sxs-lookup"><span data-stu-id="aaeef-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="aaeef-115">參數</span><span class="sxs-lookup"><span data-stu-id="aaeef-115">PARAMETERS</span></span>

### <span data-ttu-id="aaeef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaeef-116">-AsJob</span></span>
<span data-ttu-id="aaeef-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aaeef-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aaeef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaeef-118">-DefaultProfile</span></span>
<span data-ttu-id="aaeef-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aaeef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaeef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaeef-120">-InputObject</span></span>
<span data-ttu-id="aaeef-121">SyncGroup 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="aaeef-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="aaeef-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="aaeef-122">-Name</span></span>
<span data-ttu-id="aaeef-123">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaeef-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="aaeef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaeef-124">-PassThru</span></span>
<span data-ttu-id="aaeef-125">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aaeef-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="aaeef-126">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="aaeef-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="aaeef-127">-模式</span><span class="sxs-lookup"><span data-stu-id="aaeef-127">-Pattern</span></span>
<span data-ttu-id="aaeef-128">檔案名的模式</span><span class="sxs-lookup"><span data-stu-id="aaeef-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="aaeef-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="aaeef-129">-RecallPath</span></span>
<span data-ttu-id="aaeef-130">召回需要召回的路徑。</span><span class="sxs-lookup"><span data-stu-id="aaeef-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="aaeef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaeef-131">-ResourceGroupName</span></span>
<span data-ttu-id="aaeef-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="aaeef-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="aaeef-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaeef-133">-ResourceId</span></span>
<span data-ttu-id="aaeef-134">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="aaeef-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="aaeef-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="aaeef-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="aaeef-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaeef-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="aaeef-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="aaeef-137">-SyncGroupName</span></span>
<span data-ttu-id="aaeef-138">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaeef-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="aaeef-139">-確認</span><span class="sxs-lookup"><span data-stu-id="aaeef-139">-Confirm</span></span>
<span data-ttu-id="aaeef-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aaeef-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaeef-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaeef-141">-WhatIf</span></span>
<span data-ttu-id="aaeef-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aaeef-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaeef-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aaeef-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaeef-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaeef-144">CommonParameters</span></span>
<span data-ttu-id="aaeef-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aaeef-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaeef-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aaeef-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaeef-147">輸入</span><span class="sxs-lookup"><span data-stu-id="aaeef-147">INPUTS</span></span>

### <span data-ttu-id="aaeef-148">System.object</span><span class="sxs-lookup"><span data-stu-id="aaeef-148">System.String</span></span>

### <span data-ttu-id="aaeef-149">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="aaeef-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="aaeef-150">輸出</span><span class="sxs-lookup"><span data-stu-id="aaeef-150">OUTPUTS</span></span>

### <span data-ttu-id="aaeef-151">System.object</span><span class="sxs-lookup"><span data-stu-id="aaeef-151">System.Boolean</span></span>

## <span data-ttu-id="aaeef-152">筆記</span><span class="sxs-lookup"><span data-stu-id="aaeef-152">NOTES</span></span>

## <span data-ttu-id="aaeef-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaeef-153">RELATED LINKS</span></span>
