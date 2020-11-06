---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614428"
---
# <span data-ttu-id="7d637-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7d637-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="7d637-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d637-102">SYNOPSIS</span></span>
<span data-ttu-id="7d637-103">這個命令會在資源群組中建立新的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="7d637-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="7d637-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d637-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d637-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d637-105">DESCRIPTION</span></span>
<span data-ttu-id="7d637-106">儲存同步處理服務是 Azure 檔案同步處理的頂層資源。這個命令會在資源群組中建立新的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="7d637-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="7d637-107">我們建議您建立足夠的儲存同步處理服務，以完全區別貴組織中不同的伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="7d637-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="7d637-108">儲存同步處理服務包含同步群組，也會做為註冊您伺服器的目標。</span><span class="sxs-lookup"><span data-stu-id="7d637-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="7d637-109">伺服器只能註冊到單一儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="7d637-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="7d637-110">如果伺服器需要參與同步處理相同的檔案集，請將它們註冊至相同的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="7d637-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="7d637-111">示例</span><span class="sxs-lookup"><span data-stu-id="7d637-111">EXAMPLES</span></span>

### <span data-ttu-id="7d637-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7d637-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="7d637-113">這個命令會建立儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="7d637-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="7d637-114">參數</span><span class="sxs-lookup"><span data-stu-id="7d637-114">PARAMETERS</span></span>

### <span data-ttu-id="7d637-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d637-115">-DefaultProfile</span></span>
<span data-ttu-id="7d637-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d637-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d637-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7d637-117">-Location</span></span>
<span data-ttu-id="7d637-118">儲存同步處理服務位置。</span><span class="sxs-lookup"><span data-stu-id="7d637-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d637-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d637-119">-Name</span></span>
<span data-ttu-id="7d637-120">儲存空間同步處理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d637-120">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d637-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d637-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d637-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7d637-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d637-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d637-123">-Tag</span></span>
<span data-ttu-id="7d637-124">儲存同步處理服務標記。</span><span class="sxs-lookup"><span data-stu-id="7d637-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d637-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d637-125">CommonParameters</span></span>
<span data-ttu-id="7d637-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d637-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d637-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d637-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d637-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7d637-128">INPUTS</span></span>

### <span data-ttu-id="7d637-129">System.object</span><span class="sxs-lookup"><span data-stu-id="7d637-129">System.String</span></span>

## <span data-ttu-id="7d637-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7d637-130">OUTPUTS</span></span>

### <span data-ttu-id="7d637-131">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="7d637-131">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="7d637-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7d637-132">NOTES</span></span>

## <span data-ttu-id="7d637-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d637-133">RELATED LINKS</span></span>
