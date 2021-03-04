---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 53ee755daeb0e483b98c9e8449720acce6e38233
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907213"
---
# <span data-ttu-id="39bb7-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="39bb7-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="39bb7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="39bb7-103">此命令會列出給定儲存同步服務內的所有同步群組。</span><span class="sxs-lookup"><span data-stu-id="39bb7-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="39bb7-104">語法</span><span class="sxs-lookup"><span data-stu-id="39bb7-104">SYNTAX</span></span>

### <span data-ttu-id="39bb7-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="39bb7-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39bb7-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39bb7-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39bb7-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="39bb7-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39bb7-108">描述</span><span class="sxs-lookup"><span data-stu-id="39bb7-108">DESCRIPTION</span></span>
<span data-ttu-id="39bb7-109">此命令會列出給定儲存同步服務內的所有同步群組。</span><span class="sxs-lookup"><span data-stu-id="39bb7-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="39bb7-110">它可以用來列出每個同步組的屬性。</span><span class="sxs-lookup"><span data-stu-id="39bb7-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="39bb7-111">例子</span><span class="sxs-lookup"><span data-stu-id="39bb7-111">EXAMPLES</span></span>

### <span data-ttu-id="39bb7-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="39bb7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="39bb7-113">此命令會獲得指定儲存同步服務中包含的所有同步群組。</span><span class="sxs-lookup"><span data-stu-id="39bb7-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="39bb7-114">指定 -Name 以返回特定名稱。</span><span class="sxs-lookup"><span data-stu-id="39bb7-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="39bb7-115">參數</span><span class="sxs-lookup"><span data-stu-id="39bb7-115">PARAMETERS</span></span>

### <span data-ttu-id="39bb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bb7-116">-DefaultProfile</span></span>
<span data-ttu-id="39bb7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39bb7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39bb7-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="39bb7-118">-Name</span></span>
<span data-ttu-id="39bb7-119">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39bb7-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="39bb7-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39bb7-120">-ParentObject</span></span>
<span data-ttu-id="39bb7-121">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="39bb7-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="39bb7-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="39bb7-122">-ParentResourceId</span></span>
<span data-ttu-id="39bb7-123">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="39bb7-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="39bb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39bb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="39bb7-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="39bb7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="39bb7-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="39bb7-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="39bb7-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="39bb7-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="39bb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bb7-128">CommonParameters</span></span>
<span data-ttu-id="39bb7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39bb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bb7-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="39bb7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bb7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="39bb7-131">INPUTS</span></span>

### <span data-ttu-id="39bb7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="39bb7-132">System.String</span></span>

### <span data-ttu-id="39bb7-133">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="39bb7-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="39bb7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="39bb7-134">OUTPUTS</span></span>

### <span data-ttu-id="39bb7-135">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="39bb7-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="39bb7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="39bb7-136">NOTES</span></span>

## <span data-ttu-id="39bb7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="39bb7-137">RELATED LINKS</span></span>
