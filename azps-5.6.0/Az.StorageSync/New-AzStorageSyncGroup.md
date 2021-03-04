---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916852"
---
# <span data-ttu-id="00f9c-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="00f9c-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="00f9c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="00f9c-103">此命令會于指定的儲存同步服務中建立新同步組。</span><span class="sxs-lookup"><span data-stu-id="00f9c-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="00f9c-104">語法</span><span class="sxs-lookup"><span data-stu-id="00f9c-104">SYNTAX</span></span>

### <span data-ttu-id="00f9c-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="00f9c-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00f9c-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00f9c-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00f9c-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="00f9c-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00f9c-108">描述</span><span class="sxs-lookup"><span data-stu-id="00f9c-108">DESCRIPTION</span></span>
<span data-ttu-id="00f9c-109">此命令會于指定的儲存同步服務中建立新同步組。</span><span class="sxs-lookup"><span data-stu-id="00f9c-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="00f9c-110">同步處理群組是用來描述位置的拓撲 ，稱為端點，可同步處理任何儲存在任何一個端點內的檔案。</span><span class="sxs-lookup"><span data-stu-id="00f9c-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="00f9c-111">同步處理群組包含參照 Azure 檔案共用之雲端端點，同時也包含參照已登錄伺服器上特定本地路徑的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="00f9c-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="00f9c-112">例子</span><span class="sxs-lookup"><span data-stu-id="00f9c-112">EXAMPLES</span></span>

### <span data-ttu-id="00f9c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="00f9c-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="00f9c-114">此命令會于指定的儲存同步服務中建立新同步組。</span><span class="sxs-lookup"><span data-stu-id="00f9c-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="00f9c-115">參數</span><span class="sxs-lookup"><span data-stu-id="00f9c-115">PARAMETERS</span></span>

### <span data-ttu-id="00f9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f9c-116">-DefaultProfile</span></span>
<span data-ttu-id="00f9c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00f9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f9c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="00f9c-118">-Name</span></span>
<span data-ttu-id="00f9c-119">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00f9c-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="00f9c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="00f9c-120">-ParentObject</span></span>
<span data-ttu-id="00f9c-121">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="00f9c-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="00f9c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="00f9c-122">-ParentResourceId</span></span>
<span data-ttu-id="00f9c-123">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="00f9c-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="00f9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="00f9c-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="00f9c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="00f9c-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="00f9c-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="00f9c-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="00f9c-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="00f9c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="00f9c-128">-Confirm</span></span>
<span data-ttu-id="00f9c-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00f9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00f9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f9c-130">-WhatIf</span></span>
<span data-ttu-id="00f9c-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00f9c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00f9c-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00f9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00f9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f9c-133">CommonParameters</span></span>
<span data-ttu-id="00f9c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00f9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f9c-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00f9c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f9c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="00f9c-136">INPUTS</span></span>

### <span data-ttu-id="00f9c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="00f9c-137">System.String</span></span>

### <span data-ttu-id="00f9c-138">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="00f9c-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="00f9c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="00f9c-139">OUTPUTS</span></span>

### <span data-ttu-id="00f9c-140">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="00f9c-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="00f9c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="00f9c-141">NOTES</span></span>

## <span data-ttu-id="00f9c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="00f9c-142">RELATED LINKS</span></span>
