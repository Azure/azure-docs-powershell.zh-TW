---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435852"
---
# <span data-ttu-id="987f0-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="987f0-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="987f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="987f0-102">SYNOPSIS</span></span>
<span data-ttu-id="987f0-103">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="987f0-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="987f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="987f0-104">SYNTAX</span></span>

### <span data-ttu-id="987f0-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="987f0-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="987f0-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="987f0-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="987f0-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="987f0-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="987f0-108">說明</span><span class="sxs-lookup"><span data-stu-id="987f0-108">DESCRIPTION</span></span>
<span data-ttu-id="987f0-109">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="987f0-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="987f0-110">同步處理群組可用來描述將儲存在任何一個端點中之檔案的位置拓撲，稱為端點。</span><span class="sxs-lookup"><span data-stu-id="987f0-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="987f0-111">同步處理群組包含參照 Azure 檔案共用的雲端端點，也包含在已註冊的伺服器上參照特定本機路徑的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="987f0-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="987f0-112">示例</span><span class="sxs-lookup"><span data-stu-id="987f0-112">EXAMPLES</span></span>

### <span data-ttu-id="987f0-113">範例1</span><span class="sxs-lookup"><span data-stu-id="987f0-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="987f0-114">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="987f0-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="987f0-115">參數</span><span class="sxs-lookup"><span data-stu-id="987f0-115">PARAMETERS</span></span>

### <span data-ttu-id="987f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987f0-116">-DefaultProfile</span></span>
<span data-ttu-id="987f0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="987f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987f0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="987f0-118">-Name</span></span>
<span data-ttu-id="987f0-119">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="987f0-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987f0-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="987f0-120">-ParentObject</span></span>
<span data-ttu-id="987f0-121">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="987f0-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="987f0-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="987f0-122">-ParentResourceId</span></span>
<span data-ttu-id="987f0-123">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="987f0-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="987f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="987f0-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="987f0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="987f0-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="987f0-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="987f0-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="987f0-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="987f0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="987f0-128">-Confirm</span></span>
<span data-ttu-id="987f0-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="987f0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="987f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="987f0-130">-WhatIf</span></span>
<span data-ttu-id="987f0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="987f0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="987f0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="987f0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="987f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987f0-133">CommonParameters</span></span>
<span data-ttu-id="987f0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="987f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987f0-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="987f0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987f0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="987f0-136">INPUTS</span></span>

### <span data-ttu-id="987f0-137">System.object</span><span class="sxs-lookup"><span data-stu-id="987f0-137">System.String</span></span>

### <span data-ttu-id="987f0-138">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="987f0-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="987f0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="987f0-139">OUTPUTS</span></span>

### <span data-ttu-id="987f0-140">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="987f0-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="987f0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="987f0-141">NOTES</span></span>

## <span data-ttu-id="987f0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="987f0-142">RELATED LINKS</span></span>
