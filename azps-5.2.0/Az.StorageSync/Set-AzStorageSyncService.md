---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283304"
---
# <span data-ttu-id="81cac-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="81cac-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="81cac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81cac-102">SYNOPSIS</span></span>
<span data-ttu-id="81cac-103">這個命令會設定資源群組中的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="81cac-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="81cac-104">句法</span><span class="sxs-lookup"><span data-stu-id="81cac-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cac-105">說明</span><span class="sxs-lookup"><span data-stu-id="81cac-105">DESCRIPTION</span></span>
<span data-ttu-id="81cac-106">儲存同步處理服務是 Azure 檔案同步處理的頂層資源。這個命令會設定資源群組中的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="81cac-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="81cac-107">我們建議您建立足夠的儲存同步處理服務，以完全區別貴組織中不同的伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="81cac-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="81cac-108">儲存同步處理服務包含同步群組，也會做為註冊您伺服器的目標。</span><span class="sxs-lookup"><span data-stu-id="81cac-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="81cac-109">伺服器只能註冊到單一儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="81cac-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="81cac-110">如果伺服器需要參與同步處理相同的檔案集，請將它們註冊至相同的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="81cac-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="81cac-111">示例</span><span class="sxs-lookup"><span data-stu-id="81cac-111">EXAMPLES</span></span>

### <span data-ttu-id="81cac-112">範例1</span><span class="sxs-lookup"><span data-stu-id="81cac-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="81cac-113">這個命令會設定儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="81cac-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="81cac-114">參數</span><span class="sxs-lookup"><span data-stu-id="81cac-114">PARAMETERS</span></span>

### <span data-ttu-id="81cac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cac-115">-DefaultProfile</span></span>
<span data-ttu-id="81cac-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81cac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="81cac-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="81cac-117">-Name</span></span>
<span data-ttu-id="81cac-118">儲存空間同步處理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="81cac-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="81cac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cac-119">-ResourceGroupName</span></span>
<span data-ttu-id="81cac-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="81cac-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="81cac-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="81cac-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="81cac-122">儲存同步處理服務 IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="81cac-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="81cac-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="81cac-123">-Tag</span></span>
<span data-ttu-id="81cac-124">儲存同步處理服務標記。</span><span class="sxs-lookup"><span data-stu-id="81cac-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="81cac-125">-確認</span><span class="sxs-lookup"><span data-stu-id="81cac-125">-Confirm</span></span>
<span data-ttu-id="81cac-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81cac-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81cac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cac-127">-WhatIf</span></span>
<span data-ttu-id="81cac-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81cac-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81cac-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81cac-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81cac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cac-130">CommonParameters</span></span>
<span data-ttu-id="81cac-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81cac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cac-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81cac-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cac-133">輸入</span><span class="sxs-lookup"><span data-stu-id="81cac-133">INPUTS</span></span>

### <span data-ttu-id="81cac-134">System.object</span><span class="sxs-lookup"><span data-stu-id="81cac-134">System.String</span></span>

## <span data-ttu-id="81cac-135">輸出</span><span class="sxs-lookup"><span data-stu-id="81cac-135">OUTPUTS</span></span>

### <span data-ttu-id="81cac-136">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="81cac-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="81cac-137">筆記</span><span class="sxs-lookup"><span data-stu-id="81cac-137">NOTES</span></span>

## <span data-ttu-id="81cac-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="81cac-138">RELATED LINKS</span></span>
