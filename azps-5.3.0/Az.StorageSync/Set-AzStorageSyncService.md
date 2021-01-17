---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435835"
---
# <span data-ttu-id="c0c4c-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c0c4c-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="c0c4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c4c-103">這個命令會設定資源群組中的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="c0c4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0c4c-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c4c-106">儲存同步處理服務是 Azure 檔案同步處理的頂層資源。這個命令會設定資源群組中的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="c0c4c-107">我們建議您建立足夠的儲存同步處理服務，以完全區別貴組織中不同的伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="c0c4c-108">儲存同步處理服務包含同步群組，也會做為註冊您伺服器的目標。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="c0c4c-109">伺服器只能註冊到單一儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="c0c4c-110">如果伺服器需要參與同步處理相同的檔案集，請將它們註冊至相同的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="c0c4c-111">示例</span><span class="sxs-lookup"><span data-stu-id="c0c4c-111">EXAMPLES</span></span>

### <span data-ttu-id="c0c4c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c0c4c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="c0c4c-113">這個命令會設定儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="c0c4c-114">參數</span><span class="sxs-lookup"><span data-stu-id="c0c4c-114">PARAMETERS</span></span>

### <span data-ttu-id="c0c4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c4c-115">-DefaultProfile</span></span>
<span data-ttu-id="c0c4c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="c0c4c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0c4c-117">-Name</span></span>
<span data-ttu-id="c0c4c-118">儲存空間同步處理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="c0c4c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c4c-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0c4c-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="c0c4c-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="c0c4c-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="c0c4c-122">儲存同步處理服務 IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="c0c4c-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="c0c4c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0c4c-123">-Tag</span></span>
<span data-ttu-id="c0c4c-124">儲存同步處理服務標記。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="c0c4c-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c0c4c-125">-Confirm</span></span>
<span data-ttu-id="c0c4c-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c4c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c4c-127">-WhatIf</span></span>
<span data-ttu-id="c0c4c-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0c4c-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c4c-130">CommonParameters</span></span>
<span data-ttu-id="c0c4c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c4c-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c4c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c0c4c-133">INPUTS</span></span>

### <span data-ttu-id="c0c4c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="c0c4c-134">System.String</span></span>

## <span data-ttu-id="c0c4c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c0c4c-135">OUTPUTS</span></span>

### <span data-ttu-id="c0c4c-136">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="c0c4c-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c0c4c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c0c4c-137">NOTES</span></span>

## <span data-ttu-id="c0c4c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0c4c-138">RELATED LINKS</span></span>
