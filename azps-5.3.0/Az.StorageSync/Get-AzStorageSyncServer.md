---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285988"
---
# <span data-ttu-id="a54ae-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="a54ae-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="a54ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a54ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a54ae-103">這個命令會列出已登錄至特定儲存同步處理服務的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a54ae-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="a54ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="a54ae-104">SYNTAX</span></span>

### <span data-ttu-id="a54ae-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a54ae-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a54ae-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a54ae-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a54ae-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a54ae-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a54ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="a54ae-108">DESCRIPTION</span></span>
<span data-ttu-id="a54ae-109">這個命令會列出已登錄至特定儲存同步處理服務的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a54ae-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="a54ae-110">您也可以使用它來列出每個已登錄伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="a54ae-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="a54ae-111">示例</span><span class="sxs-lookup"><span data-stu-id="a54ae-111">EXAMPLES</span></span>

### <span data-ttu-id="a54ae-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a54ae-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="a54ae-113">這個命令會取得已登錄至特定儲存同步處理服務的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a54ae-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="a54ae-114">參數</span><span class="sxs-lookup"><span data-stu-id="a54ae-114">PARAMETERS</span></span>

### <span data-ttu-id="a54ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54ae-115">-DefaultProfile</span></span>
<span data-ttu-id="a54ae-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a54ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54ae-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a54ae-117">-ParentObject</span></span>
<span data-ttu-id="a54ae-118">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="a54ae-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a54ae-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a54ae-119">-ParentResourceId</span></span>
<span data-ttu-id="a54ae-120">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="a54ae-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a54ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="a54ae-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a54ae-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="a54ae-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="a54ae-123">-ServerId</span></span>
<span data-ttu-id="a54ae-124">RegisteredServer 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a54ae-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="a54ae-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a54ae-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="a54ae-126">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a54ae-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a54ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54ae-127">CommonParameters</span></span>
<span data-ttu-id="a54ae-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a54ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54ae-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a54ae-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54ae-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a54ae-130">INPUTS</span></span>

### <span data-ttu-id="a54ae-131">System.object</span><span class="sxs-lookup"><span data-stu-id="a54ae-131">System.String</span></span>

### <span data-ttu-id="a54ae-132">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="a54ae-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="a54ae-133">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="a54ae-133">System.Guid</span></span>

## <span data-ttu-id="a54ae-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a54ae-134">OUTPUTS</span></span>

### <span data-ttu-id="a54ae-135">PSRegisteredServer 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="a54ae-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="a54ae-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a54ae-136">NOTES</span></span>

## <span data-ttu-id="a54ae-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a54ae-137">RELATED LINKS</span></span>
