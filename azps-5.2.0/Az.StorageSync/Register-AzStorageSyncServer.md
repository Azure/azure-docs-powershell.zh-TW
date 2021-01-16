---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283328"
---
# <span data-ttu-id="abe93-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="abe93-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="abe93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abe93-102">SYNOPSIS</span></span>
<span data-ttu-id="abe93-103">這個命令會將伺服器註冊至儲存同步處理服務，這會建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="abe93-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="abe93-104">然後，您可以使用 PowerShell 或 Azure 入口網站來設定此伺服器上的同步處理。</span><span class="sxs-lookup"><span data-stu-id="abe93-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="abe93-105">句法</span><span class="sxs-lookup"><span data-stu-id="abe93-105">SYNTAX</span></span>

### <span data-ttu-id="abe93-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="abe93-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe93-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abe93-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe93-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="abe93-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe93-109">說明</span><span class="sxs-lookup"><span data-stu-id="abe93-109">DESCRIPTION</span></span>
<span data-ttu-id="abe93-110">這個命令會將伺服器註冊至儲存同步服務，即 Azure 檔案同步處理的頂層資源。已建立伺服器與儲存同步處理服務之間的信任關係，以確保安全的資料傳輸與管理通道。</span><span class="sxs-lookup"><span data-stu-id="abe93-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="abe93-111">然後，您可以使用 PowerShell 或 Azure 入口網站來設定此伺服器上的同步處理。</span><span class="sxs-lookup"><span data-stu-id="abe93-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="abe93-112">伺服器只能註冊到單一儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="abe93-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="abe93-113">如果伺服器需要參與同步處理相同的檔案集，請將它們註冊至相同的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="abe93-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="abe93-114">此命令必須在要登錄的伺服器上以本機方式執行，要麼直接執行，要麼透過遠端 PowerShell 會話執行。</span><span class="sxs-lookup"><span data-stu-id="abe93-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="abe93-115">無法接受遠端電腦物件。</span><span class="sxs-lookup"><span data-stu-id="abe93-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="abe93-116">示例</span><span class="sxs-lookup"><span data-stu-id="abe93-116">EXAMPLES</span></span>

### <span data-ttu-id="abe93-117">範例1</span><span class="sxs-lookup"><span data-stu-id="abe93-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="abe93-118">這個命令會註冊本機伺服器，此命令是在上執行。</span><span class="sxs-lookup"><span data-stu-id="abe93-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="abe93-119">參數</span><span class="sxs-lookup"><span data-stu-id="abe93-119">PARAMETERS</span></span>

### <span data-ttu-id="abe93-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abe93-120">-AsJob</span></span>
<span data-ttu-id="abe93-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="abe93-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abe93-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe93-122">-DefaultProfile</span></span>
<span data-ttu-id="abe93-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="abe93-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abe93-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="abe93-124">-ParentObject</span></span>
<span data-ttu-id="abe93-125">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="abe93-125">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abe93-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="abe93-126">-ParentResourceId</span></span>
<span data-ttu-id="abe93-127">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="abe93-127">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe93-128">-ResourceGroupName</span></span>
<span data-ttu-id="abe93-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="abe93-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe93-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="abe93-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="abe93-131">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="abe93-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe93-132">-確認</span><span class="sxs-lookup"><span data-stu-id="abe93-132">-Confirm</span></span>
<span data-ttu-id="abe93-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="abe93-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe93-134">-WhatIf</span></span>
<span data-ttu-id="abe93-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abe93-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abe93-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abe93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe93-137">CommonParameters</span></span>
<span data-ttu-id="abe93-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abe93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe93-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abe93-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe93-140">輸入</span><span class="sxs-lookup"><span data-stu-id="abe93-140">INPUTS</span></span>

### <span data-ttu-id="abe93-141">System.object</span><span class="sxs-lookup"><span data-stu-id="abe93-141">System.String</span></span>

### <span data-ttu-id="abe93-142">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="abe93-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="abe93-143">輸出</span><span class="sxs-lookup"><span data-stu-id="abe93-143">OUTPUTS</span></span>

### <span data-ttu-id="abe93-144">PSRegisteredServer 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="abe93-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="abe93-145">筆記</span><span class="sxs-lookup"><span data-stu-id="abe93-145">NOTES</span></span>

## <span data-ttu-id="abe93-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="abe93-146">RELATED LINKS</span></span>
