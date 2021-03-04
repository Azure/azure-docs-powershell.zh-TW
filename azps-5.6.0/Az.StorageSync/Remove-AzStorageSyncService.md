---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907426"
---
# <span data-ttu-id="31993-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="31993-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="31993-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31993-102">SYNOPSIS</span></span>
<span data-ttu-id="31993-103">此命令將會刪除指定的儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="31993-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="31993-104">語法</span><span class="sxs-lookup"><span data-stu-id="31993-104">SYNTAX</span></span>

### <span data-ttu-id="31993-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="31993-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31993-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31993-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31993-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31993-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31993-108">描述</span><span class="sxs-lookup"><span data-stu-id="31993-108">DESCRIPTION</span></span>
<span data-ttu-id="31993-109">此命令將會刪除指定的儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="31993-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="31993-110">儲存同步處理服務只有在先刪除所有包含的同步處理群組和登錄伺服器時才能移除。</span><span class="sxs-lookup"><span data-stu-id="31993-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="31993-111">例子</span><span class="sxs-lookup"><span data-stu-id="31993-111">EXAMPLES</span></span>

### <span data-ttu-id="31993-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="31993-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="31993-113">此命令會移除儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="31993-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="31993-114">參數</span><span class="sxs-lookup"><span data-stu-id="31993-114">PARAMETERS</span></span>

### <span data-ttu-id="31993-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31993-115">-AsJob</span></span>
<span data-ttu-id="31993-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="31993-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31993-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31993-117">-DefaultProfile</span></span>
<span data-ttu-id="31993-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31993-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31993-119">-強制</span><span class="sxs-lookup"><span data-stu-id="31993-119">-Force</span></span>
<span data-ttu-id="31993-120">提供 -強制跳過此命令的確認。</span><span class="sxs-lookup"><span data-stu-id="31993-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="31993-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31993-121">-InputObject</span></span>
<span data-ttu-id="31993-122">StorageSyncService 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="31993-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="31993-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="31993-123">-Name</span></span>
<span data-ttu-id="31993-124">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="31993-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="31993-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31993-125">-PassThru</span></span>
<span data-ttu-id="31993-126">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="31993-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="31993-127">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="31993-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="31993-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31993-128">-ResourceGroupName</span></span>
<span data-ttu-id="31993-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="31993-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="31993-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31993-130">-ResourceId</span></span>
<span data-ttu-id="31993-131">StorageSyncService 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="31993-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="31993-132">-確認</span><span class="sxs-lookup"><span data-stu-id="31993-132">-Confirm</span></span>
<span data-ttu-id="31993-133">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31993-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31993-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31993-134">-WhatIf</span></span>
<span data-ttu-id="31993-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31993-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31993-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31993-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31993-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31993-137">CommonParameters</span></span>
<span data-ttu-id="31993-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31993-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31993-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="31993-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31993-140">輸入</span><span class="sxs-lookup"><span data-stu-id="31993-140">INPUTS</span></span>

### <span data-ttu-id="31993-141">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="31993-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="31993-142">System.String</span><span class="sxs-lookup"><span data-stu-id="31993-142">System.String</span></span>

### <span data-ttu-id="31993-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31993-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31993-144">輸出</span><span class="sxs-lookup"><span data-stu-id="31993-144">OUTPUTS</span></span>

### <span data-ttu-id="31993-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="31993-145">System.Object</span></span>
## <span data-ttu-id="31993-146">筆記</span><span class="sxs-lookup"><span data-stu-id="31993-146">NOTES</span></span>

## <span data-ttu-id="31993-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="31993-147">RELATED LINKS</span></span>
