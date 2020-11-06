---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614435"
---
# <span data-ttu-id="bbc9f-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="bbc9f-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="bbc9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc9f-103">這個命令會將所有的分層檔案撤回回本機磁片。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="bbc9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbc9f-104">SYNTAX</span></span>

### <span data-ttu-id="bbc9f-105">ObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bbc9f-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbc9f-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc9f-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbc9f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc9f-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbc9f-108">說明</span><span class="sxs-lookup"><span data-stu-id="bbc9f-108">DESCRIPTION</span></span>
<span data-ttu-id="bbc9f-109">在伺服器端點上啟用雲端分層之後 (在已登錄伺服器上的特定位置) ，就可以使用此命令，將所有的分層檔案撤回到本機磁片。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="bbc9f-110">強烈建議您先在此伺服器端點上停用雲端堆疊，然後再開始撤回。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="bbc9f-111">如果堆疊仍開啟，則召回可能會導致其他檔案在進行分級，以達到在本機磁片上的所有內容所需的目標。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="bbc9f-112">示例</span><span class="sxs-lookup"><span data-stu-id="bbc9f-112">EXAMPLES</span></span>

### <span data-ttu-id="bbc9f-113">範例1</span><span class="sxs-lookup"><span data-stu-id="bbc9f-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="bbc9f-114">這個命令會以遞迴方式，撤回位於指定伺服器端點之根路徑下的所有分層檔案。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="bbc9f-115">參數</span><span class="sxs-lookup"><span data-stu-id="bbc9f-115">PARAMETERS</span></span>

### <span data-ttu-id="bbc9f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbc9f-116">-AsJob</span></span>
<span data-ttu-id="bbc9f-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bbc9f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbc9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc9f-118">-DefaultProfile</span></span>
<span data-ttu-id="bbc9f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbc9f-120">-InputObject</span></span>
<span data-ttu-id="bbc9f-121">SyncGroup 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc9f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbc9f-122">-Name</span></span>
<span data-ttu-id="bbc9f-123">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="bbc9f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbc9f-124">-PassThru</span></span>
<span data-ttu-id="bbc9f-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="bbc9f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bbc9f-126">-模式</span><span class="sxs-lookup"><span data-stu-id="bbc9f-126">-Pattern</span></span>
<span data-ttu-id="bbc9f-127">檔案名的模式</span><span class="sxs-lookup"><span data-stu-id="bbc9f-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="bbc9f-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="bbc9f-128">-RecallPath</span></span>
<span data-ttu-id="bbc9f-129">召回需要召回的路徑。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="bbc9f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc9f-130">-ResourceGroupName</span></span>
<span data-ttu-id="bbc9f-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="bbc9f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbc9f-132">-ResourceId</span></span>
<span data-ttu-id="bbc9f-133">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bbc9f-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="bbc9f-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="bbc9f-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="bbc9f-135">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="bbc9f-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc9f-136">-SyncGroupName</span></span>
<span data-ttu-id="bbc9f-137">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="bbc9f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc9f-138">CommonParameters</span></span>
<span data-ttu-id="bbc9f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc9f-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc9f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="bbc9f-141">INPUTS</span></span>

### <span data-ttu-id="bbc9f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bbc9f-142">System.String</span></span>

### <span data-ttu-id="bbc9f-143">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="bbc9f-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="bbc9f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bbc9f-144">OUTPUTS</span></span>

### <span data-ttu-id="bbc9f-145">System.object</span><span class="sxs-lookup"><span data-stu-id="bbc9f-145">System.Boolean</span></span>

## <span data-ttu-id="bbc9f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bbc9f-146">NOTES</span></span>

## <span data-ttu-id="bbc9f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbc9f-147">RELATED LINKS</span></span>
