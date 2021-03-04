---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: 62dcefcf48e1d4c685b2a4f4855af41da7d8db75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916841"
---
# <span data-ttu-id="71a9b-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="71a9b-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="71a9b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="71a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="71a9b-103">此命令會註冊伺服器至儲存同步處理服務，服務會建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="71a9b-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="71a9b-104">PowerShell 或 Azure 入口網站之後，就可以在此伺服器上設定同步處理。</span><span class="sxs-lookup"><span data-stu-id="71a9b-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="71a9b-105">語法</span><span class="sxs-lookup"><span data-stu-id="71a9b-105">SYNTAX</span></span>

### <span data-ttu-id="71a9b-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71a9b-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a9b-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71a9b-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a9b-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="71a9b-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a9b-109">描述</span><span class="sxs-lookup"><span data-stu-id="71a9b-109">DESCRIPTION</span></span>
<span data-ttu-id="71a9b-110">此命令會註冊伺服器至儲存空間同步處理服務，這是 Azure 檔案同步處理的頂層資源。伺服器與儲存空間同步處理服務之間的信任關係會建立，以確保安全的資料傳輸和管理通道。</span><span class="sxs-lookup"><span data-stu-id="71a9b-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="71a9b-111">PowerShell 或 Azure 入口網站就可以用來設定此伺服器上同步處理的內容。</span><span class="sxs-lookup"><span data-stu-id="71a9b-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="71a9b-112">伺服器只能註冊單一儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="71a9b-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="71a9b-113">如果伺服器需要參與同步處理同一組檔案，請將它們註冊到相同的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="71a9b-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="71a9b-114">該命令必須在要登錄的伺服器上于本地執行，無論是直接執行或透過遠端 PowerShell 會話執行。</span><span class="sxs-lookup"><span data-stu-id="71a9b-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="71a9b-115">遠端電腦物件無法接受。</span><span class="sxs-lookup"><span data-stu-id="71a9b-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="71a9b-116">例子</span><span class="sxs-lookup"><span data-stu-id="71a9b-116">EXAMPLES</span></span>

### <span data-ttu-id="71a9b-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="71a9b-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="71a9b-118">此命令會登錄執行此命令的當地伺服器。</span><span class="sxs-lookup"><span data-stu-id="71a9b-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="71a9b-119">參數</span><span class="sxs-lookup"><span data-stu-id="71a9b-119">PARAMETERS</span></span>

### <span data-ttu-id="71a9b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71a9b-120">-AsJob</span></span>
<span data-ttu-id="71a9b-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71a9b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71a9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a9b-122">-DefaultProfile</span></span>
<span data-ttu-id="71a9b-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="71a9b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a9b-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="71a9b-124">-ParentObject</span></span>
<span data-ttu-id="71a9b-125">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="71a9b-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="71a9b-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="71a9b-126">-ParentResourceId</span></span>
<span data-ttu-id="71a9b-127">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="71a9b-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="71a9b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a9b-128">-ResourceGroupName</span></span>
<span data-ttu-id="71a9b-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="71a9b-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="71a9b-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="71a9b-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="71a9b-131">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="71a9b-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="71a9b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="71a9b-132">-Confirm</span></span>
<span data-ttu-id="71a9b-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="71a9b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a9b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a9b-134">-WhatIf</span></span>
<span data-ttu-id="71a9b-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71a9b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71a9b-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71a9b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a9b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a9b-137">CommonParameters</span></span>
<span data-ttu-id="71a9b-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="71a9b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a9b-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="71a9b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a9b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="71a9b-140">INPUTS</span></span>

### <span data-ttu-id="71a9b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="71a9b-141">System.String</span></span>

### <span data-ttu-id="71a9b-142">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="71a9b-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="71a9b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="71a9b-143">OUTPUTS</span></span>

### <span data-ttu-id="71a9b-144">Microsoft.Azure.Commands.StorageSync.models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="71a9b-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="71a9b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="71a9b-145">NOTES</span></span>

## <span data-ttu-id="71a9b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="71a9b-146">RELATED LINKS</span></span>
