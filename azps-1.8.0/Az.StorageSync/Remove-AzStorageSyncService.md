---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614417"
---
# <span data-ttu-id="093f6-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="093f6-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="093f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="093f6-102">SYNOPSIS</span></span>
<span data-ttu-id="093f6-103">這個命令會刪除指定的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="093f6-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="093f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="093f6-104">SYNTAX</span></span>

### <span data-ttu-id="093f6-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="093f6-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="093f6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="093f6-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="093f6-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="093f6-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="093f6-108">說明</span><span class="sxs-lookup"><span data-stu-id="093f6-108">DESCRIPTION</span></span>
<span data-ttu-id="093f6-109">這個命令會刪除指定的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="093f6-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="093f6-110">只有在先刪除所有包含的同步處理群組與已註冊的伺服器時，才能移除儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="093f6-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="093f6-111">示例</span><span class="sxs-lookup"><span data-stu-id="093f6-111">EXAMPLES</span></span>

### <span data-ttu-id="093f6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="093f6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="093f6-113">這個命令會移除儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="093f6-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="093f6-114">參數</span><span class="sxs-lookup"><span data-stu-id="093f6-114">PARAMETERS</span></span>

### <span data-ttu-id="093f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="093f6-115">-AsJob</span></span>
<span data-ttu-id="093f6-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="093f6-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093f6-117">-DefaultProfile</span></span>
<span data-ttu-id="093f6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="093f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="093f6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="093f6-119">-Force</span></span>
<span data-ttu-id="093f6-120">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="093f6-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="093f6-121">-InputObject</span></span>
<span data-ttu-id="093f6-122">StorageSyncService 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="093f6-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="093f6-123">-Name</span></span>
<span data-ttu-id="093f6-124">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="093f6-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="093f6-125">-PassThru</span></span>
<span data-ttu-id="093f6-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="093f6-126">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093f6-127">-ResourceGroupName</span></span>
<span data-ttu-id="093f6-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="093f6-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="093f6-129">-ResourceId</span></span>
<span data-ttu-id="093f6-130">StorageSyncService 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="093f6-130">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="093f6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="093f6-131">-Confirm</span></span>
<span data-ttu-id="093f6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="093f6-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093f6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093f6-133">-WhatIf</span></span>
<span data-ttu-id="093f6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="093f6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="093f6-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="093f6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093f6-136">CommonParameters</span></span>
<span data-ttu-id="093f6-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="093f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093f6-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="093f6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093f6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="093f6-139">INPUTS</span></span>

### <span data-ttu-id="093f6-140">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="093f6-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="093f6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="093f6-141">System.String</span></span>

### <span data-ttu-id="093f6-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="093f6-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="093f6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="093f6-143">OUTPUTS</span></span>

### <span data-ttu-id="093f6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="093f6-144">System.Object</span></span>
## <span data-ttu-id="093f6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="093f6-145">NOTES</span></span>

## <span data-ttu-id="093f6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="093f6-146">RELATED LINKS</span></span>
