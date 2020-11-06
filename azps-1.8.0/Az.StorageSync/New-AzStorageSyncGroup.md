---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614430"
---
# <span data-ttu-id="c2537-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c2537-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="c2537-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2537-102">SYNOPSIS</span></span>
<span data-ttu-id="c2537-103">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="c2537-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="c2537-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2537-104">SYNTAX</span></span>

### <span data-ttu-id="c2537-105">ObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2537-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2537-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2537-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2537-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2537-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2537-108">說明</span><span class="sxs-lookup"><span data-stu-id="c2537-108">DESCRIPTION</span></span>
<span data-ttu-id="c2537-109">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="c2537-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="c2537-110">同步處理群組可用來描述將儲存在任何一個端點中之檔案的位置拓撲，稱為端點。</span><span class="sxs-lookup"><span data-stu-id="c2537-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="c2537-111">同步處理群組包含參照 Azure 檔案共用的雲端端點，也包含在已註冊的伺服器上參照特定本機路徑的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="c2537-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="c2537-112">示例</span><span class="sxs-lookup"><span data-stu-id="c2537-112">EXAMPLES</span></span>

### <span data-ttu-id="c2537-113">範例1</span><span class="sxs-lookup"><span data-stu-id="c2537-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="c2537-114">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="c2537-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="c2537-115">參數</span><span class="sxs-lookup"><span data-stu-id="c2537-115">PARAMETERS</span></span>

### <span data-ttu-id="c2537-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2537-116">-DefaultProfile</span></span>
<span data-ttu-id="c2537-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2537-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2537-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2537-118">-Name</span></span>
<span data-ttu-id="c2537-119">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2537-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c2537-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2537-120">-ParentObject</span></span>
<span data-ttu-id="c2537-121">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="c2537-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c2537-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c2537-122">-ParentResourceId</span></span>
<span data-ttu-id="c2537-123">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2537-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="c2537-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2537-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2537-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c2537-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2537-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c2537-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="c2537-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2537-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c2537-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2537-128">CommonParameters</span></span>
<span data-ttu-id="c2537-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2537-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2537-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2537-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2537-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c2537-131">INPUTS</span></span>

### <span data-ttu-id="c2537-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c2537-132">System.String</span></span>

### <span data-ttu-id="c2537-133">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="c2537-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c2537-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c2537-134">OUTPUTS</span></span>

### <span data-ttu-id="c2537-135">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="c2537-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="c2537-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c2537-136">NOTES</span></span>

## <span data-ttu-id="c2537-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2537-137">RELATED LINKS</span></span>
