---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 4da44d6ecff7dbf6de9c0fb20f74988688e9826d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915002"
---
# <span data-ttu-id="11353-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="11353-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="11353-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11353-102">SYNOPSIS</span></span>
<span data-ttu-id="11353-103">此命令會回收所有分層檔案回局磁片。</span><span class="sxs-lookup"><span data-stu-id="11353-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="11353-104">語法</span><span class="sxs-lookup"><span data-stu-id="11353-104">SYNTAX</span></span>

### <span data-ttu-id="11353-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11353-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11353-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11353-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11353-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11353-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11353-108">描述</span><span class="sxs-lookup"><span data-stu-id="11353-108">DESCRIPTION</span></span>
<span data-ttu-id="11353-109">當在伺服器端點上啟用雲端 (登錄伺服器上的特定位置) 則此命令可用來將所有分層檔案回收到本地磁片。</span><span class="sxs-lookup"><span data-stu-id="11353-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="11353-110">強烈建議您先停用此伺服器端點上的雲端分層，然後再開始回收。</span><span class="sxs-lookup"><span data-stu-id="11353-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="11353-111">如果層級設定仍為上線，回收可能會導致其他檔案被分層，而未達所有位於本地磁片上之內容的目標。</span><span class="sxs-lookup"><span data-stu-id="11353-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="11353-112">例子</span><span class="sxs-lookup"><span data-stu-id="11353-112">EXAMPLES</span></span>

### <span data-ttu-id="11353-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="11353-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="11353-114">此命令會重複回收位於指定伺服器端點根路徑下的所有分層檔案。</span><span class="sxs-lookup"><span data-stu-id="11353-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="11353-115">參數</span><span class="sxs-lookup"><span data-stu-id="11353-115">PARAMETERS</span></span>

### <span data-ttu-id="11353-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11353-116">-AsJob</span></span>
<span data-ttu-id="11353-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11353-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11353-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11353-118">-DefaultProfile</span></span>
<span data-ttu-id="11353-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11353-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11353-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11353-120">-InputObject</span></span>
<span data-ttu-id="11353-121">SyncGroup 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="11353-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="11353-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="11353-122">-Name</span></span>
<span data-ttu-id="11353-123">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11353-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="11353-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11353-124">-PassThru</span></span>
<span data-ttu-id="11353-125">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="11353-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="11353-126">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="11353-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="11353-127">-模式</span><span class="sxs-lookup"><span data-stu-id="11353-127">-Pattern</span></span>
<span data-ttu-id="11353-128">檔案名的模式</span><span class="sxs-lookup"><span data-stu-id="11353-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="11353-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="11353-129">-RecallPath</span></span>
<span data-ttu-id="11353-130">需要回收的回收路徑。</span><span class="sxs-lookup"><span data-stu-id="11353-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="11353-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11353-131">-ResourceGroupName</span></span>
<span data-ttu-id="11353-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="11353-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="11353-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11353-133">-ResourceId</span></span>
<span data-ttu-id="11353-134">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="11353-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="11353-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="11353-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="11353-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11353-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="11353-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="11353-137">-SyncGroupName</span></span>
<span data-ttu-id="11353-138">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11353-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="11353-139">-確認</span><span class="sxs-lookup"><span data-stu-id="11353-139">-Confirm</span></span>
<span data-ttu-id="11353-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11353-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11353-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11353-141">-WhatIf</span></span>
<span data-ttu-id="11353-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11353-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11353-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11353-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11353-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11353-144">CommonParameters</span></span>
<span data-ttu-id="11353-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11353-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11353-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11353-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11353-147">輸入</span><span class="sxs-lookup"><span data-stu-id="11353-147">INPUTS</span></span>

### <span data-ttu-id="11353-148">System.String</span><span class="sxs-lookup"><span data-stu-id="11353-148">System.String</span></span>

### <span data-ttu-id="11353-149">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="11353-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="11353-150">輸出</span><span class="sxs-lookup"><span data-stu-id="11353-150">OUTPUTS</span></span>

### <span data-ttu-id="11353-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11353-151">System.Boolean</span></span>

## <span data-ttu-id="11353-152">筆記</span><span class="sxs-lookup"><span data-stu-id="11353-152">NOTES</span></span>

## <span data-ttu-id="11353-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="11353-153">RELATED LINKS</span></span>
