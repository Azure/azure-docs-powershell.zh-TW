---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958392"
---
# <span data-ttu-id="c43f0-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c43f0-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="c43f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c43f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c43f0-103">這個命令會列出特定儲存同步處理服務中的所有同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="c43f0-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="c43f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="c43f0-104">SYNTAX</span></span>

### <span data-ttu-id="c43f0-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c43f0-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43f0-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c43f0-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43f0-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c43f0-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c43f0-108">說明</span><span class="sxs-lookup"><span data-stu-id="c43f0-108">DESCRIPTION</span></span>
<span data-ttu-id="c43f0-109">這個命令會列出特定儲存同步處理服務中的所有同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="c43f0-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="c43f0-110">您也可以使用它來列出每個同步群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="c43f0-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="c43f0-111">示例</span><span class="sxs-lookup"><span data-stu-id="c43f0-111">EXAMPLES</span></span>

### <span data-ttu-id="c43f0-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c43f0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="c43f0-113">這個命令會取得包含在指定的儲存同步處理服務內的所有同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="c43f0-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="c43f0-114">指定-名稱以傳回特定專案。</span><span class="sxs-lookup"><span data-stu-id="c43f0-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="c43f0-115">參數</span><span class="sxs-lookup"><span data-stu-id="c43f0-115">PARAMETERS</span></span>

### <span data-ttu-id="c43f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43f0-116">-DefaultProfile</span></span>
<span data-ttu-id="c43f0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c43f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c43f0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c43f0-118">-Name</span></span>
<span data-ttu-id="c43f0-119">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c43f0-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43f0-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c43f0-120">-ParentObject</span></span>
<span data-ttu-id="c43f0-121">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="c43f0-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c43f0-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c43f0-122">-ParentResourceId</span></span>
<span data-ttu-id="c43f0-123">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="c43f0-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c43f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c43f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="c43f0-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c43f0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c43f0-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c43f0-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="c43f0-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c43f0-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c43f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43f0-128">CommonParameters</span></span>
<span data-ttu-id="c43f0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c43f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43f0-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c43f0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43f0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c43f0-131">INPUTS</span></span>

### <span data-ttu-id="c43f0-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c43f0-132">System.String</span></span>

### <span data-ttu-id="c43f0-133">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="c43f0-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c43f0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c43f0-134">OUTPUTS</span></span>

### <span data-ttu-id="c43f0-135">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="c43f0-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="c43f0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c43f0-136">NOTES</span></span>

## <span data-ttu-id="c43f0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c43f0-137">RELATED LINKS</span></span>
