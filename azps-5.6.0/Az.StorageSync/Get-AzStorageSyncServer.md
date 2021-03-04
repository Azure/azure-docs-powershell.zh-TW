---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: 525d51d62477db88da78eaecc482d6cf64dbf810
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907210"
---
# <span data-ttu-id="3d431-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3d431-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="3d431-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3d431-102">SYNOPSIS</span></span>
<span data-ttu-id="3d431-103">此命令會列出所有註冊至給定儲存同步處理服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d431-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="3d431-104">語法</span><span class="sxs-lookup"><span data-stu-id="3d431-104">SYNTAX</span></span>

### <span data-ttu-id="3d431-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3d431-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d431-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d431-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d431-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d431-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d431-108">描述</span><span class="sxs-lookup"><span data-stu-id="3d431-108">DESCRIPTION</span></span>
<span data-ttu-id="3d431-109">此命令會列出所有註冊至給定儲存同步處理服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d431-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="3d431-110">它可以用來列出每個已登錄伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="3d431-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="3d431-111">例子</span><span class="sxs-lookup"><span data-stu-id="3d431-111">EXAMPLES</span></span>

### <span data-ttu-id="3d431-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="3d431-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="3d431-113">此命令會獲得所有已註冊特定儲存同步處理服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d431-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="3d431-114">參數</span><span class="sxs-lookup"><span data-stu-id="3d431-114">PARAMETERS</span></span>

### <span data-ttu-id="3d431-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d431-115">-DefaultProfile</span></span>
<span data-ttu-id="3d431-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d431-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d431-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d431-117">-ParentObject</span></span>
<span data-ttu-id="3d431-118">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="3d431-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3d431-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3d431-119">-ParentResourceId</span></span>
<span data-ttu-id="3d431-120">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="3d431-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3d431-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d431-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d431-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3d431-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d431-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="3d431-123">-ServerId</span></span>
<span data-ttu-id="3d431-124">RegisteredServer 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d431-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d431-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3d431-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="3d431-126">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d431-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3d431-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d431-127">CommonParameters</span></span>
<span data-ttu-id="3d431-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3d431-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d431-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3d431-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d431-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3d431-130">INPUTS</span></span>

### <span data-ttu-id="3d431-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3d431-131">System.String</span></span>

### <span data-ttu-id="3d431-132">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3d431-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="3d431-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3d431-133">System.Guid</span></span>

## <span data-ttu-id="3d431-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3d431-134">OUTPUTS</span></span>

### <span data-ttu-id="3d431-135">Microsoft.Azure.Commands.StorageSync.models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="3d431-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="3d431-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3d431-136">NOTES</span></span>

## <span data-ttu-id="3d431-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d431-137">RELATED LINKS</span></span>
