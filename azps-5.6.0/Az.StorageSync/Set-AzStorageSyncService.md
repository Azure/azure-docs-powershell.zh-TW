---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: f7b3f0924b1033f1c3b4ffd773ebbbbed985fa3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907421"
---
# <span data-ttu-id="75609-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="75609-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="75609-102">簡介</span><span class="sxs-lookup"><span data-stu-id="75609-102">SYNOPSIS</span></span>
<span data-ttu-id="75609-103">此命令會設定資源群組中的儲存空間同步服務。</span><span class="sxs-lookup"><span data-stu-id="75609-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="75609-104">語法</span><span class="sxs-lookup"><span data-stu-id="75609-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75609-105">描述</span><span class="sxs-lookup"><span data-stu-id="75609-105">DESCRIPTION</span></span>
<span data-ttu-id="75609-106">儲存同步服務是 Azure 檔案同步的頂層資源。此命令會設定資源群組中的儲存空間同步服務。</span><span class="sxs-lookup"><span data-stu-id="75609-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="75609-107">建議您盡可能少建立儲存同步處理服務，以區分貴組織中不同的伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="75609-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="75609-108">儲存同步處理服務包含同步處理群組，也可以做為註冊伺服器的目標。</span><span class="sxs-lookup"><span data-stu-id="75609-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="75609-109">伺服器只能註冊單一儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="75609-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="75609-110">如果伺服器需要參與同步處理同一組檔案，請將它們註冊到相同的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="75609-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="75609-111">例子</span><span class="sxs-lookup"><span data-stu-id="75609-111">EXAMPLES</span></span>

### <span data-ttu-id="75609-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="75609-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="75609-113">此命令會設定儲存空間同步服務。</span><span class="sxs-lookup"><span data-stu-id="75609-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="75609-114">參數</span><span class="sxs-lookup"><span data-stu-id="75609-114">PARAMETERS</span></span>

### <span data-ttu-id="75609-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75609-115">-DefaultProfile</span></span>
<span data-ttu-id="75609-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="75609-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="75609-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="75609-117">-Name</span></span>
<span data-ttu-id="75609-118">儲存空間同步服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="75609-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="75609-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75609-119">-ResourceGroupName</span></span>
<span data-ttu-id="75609-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="75609-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="75609-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="75609-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="75609-122">儲存同步處理服務 IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="75609-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="75609-123">-標記</span><span class="sxs-lookup"><span data-stu-id="75609-123">-Tag</span></span>
<span data-ttu-id="75609-124">儲存空間同步服務標記。</span><span class="sxs-lookup"><span data-stu-id="75609-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75609-125">-確認</span><span class="sxs-lookup"><span data-stu-id="75609-125">-Confirm</span></span>
<span data-ttu-id="75609-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="75609-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75609-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75609-127">-WhatIf</span></span>
<span data-ttu-id="75609-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75609-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75609-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75609-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75609-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75609-130">CommonParameters</span></span>
<span data-ttu-id="75609-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="75609-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75609-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="75609-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75609-133">輸入</span><span class="sxs-lookup"><span data-stu-id="75609-133">INPUTS</span></span>

### <span data-ttu-id="75609-134">System.String</span><span class="sxs-lookup"><span data-stu-id="75609-134">System.String</span></span>

## <span data-ttu-id="75609-135">輸出</span><span class="sxs-lookup"><span data-stu-id="75609-135">OUTPUTS</span></span>

### <span data-ttu-id="75609-136">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="75609-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="75609-137">筆記</span><span class="sxs-lookup"><span data-stu-id="75609-137">NOTES</span></span>

## <span data-ttu-id="75609-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="75609-138">RELATED LINKS</span></span>
