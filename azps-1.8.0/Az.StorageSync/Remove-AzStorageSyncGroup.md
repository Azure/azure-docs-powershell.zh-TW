---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614423"
---
# <span data-ttu-id="92dbe-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="92dbe-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="92dbe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="92dbe-103">這個命令會刪除指定的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="92dbe-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="92dbe-104">句法</span><span class="sxs-lookup"><span data-stu-id="92dbe-104">SYNTAX</span></span>

### <span data-ttu-id="92dbe-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="92dbe-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92dbe-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92dbe-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92dbe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92dbe-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92dbe-108">說明</span><span class="sxs-lookup"><span data-stu-id="92dbe-108">DESCRIPTION</span></span>
<span data-ttu-id="92dbe-109">這個命令會刪除指定的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="92dbe-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="92dbe-110">只有在第一次刪除所有包含的端點時，才能移除同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="92dbe-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="92dbe-111">示例</span><span class="sxs-lookup"><span data-stu-id="92dbe-111">EXAMPLES</span></span>

### <span data-ttu-id="92dbe-112">範例1</span><span class="sxs-lookup"><span data-stu-id="92dbe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="92dbe-113">這個命令會移除 [同步處理] 群組。</span><span class="sxs-lookup"><span data-stu-id="92dbe-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="92dbe-114">參數</span><span class="sxs-lookup"><span data-stu-id="92dbe-114">PARAMETERS</span></span>

### <span data-ttu-id="92dbe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92dbe-115">-AsJob</span></span>
<span data-ttu-id="92dbe-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="92dbe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92dbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92dbe-117">-DefaultProfile</span></span>
<span data-ttu-id="92dbe-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92dbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92dbe-119">-Force</span><span class="sxs-lookup"><span data-stu-id="92dbe-119">-Force</span></span>
<span data-ttu-id="92dbe-120">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="92dbe-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="92dbe-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92dbe-121">-InputObject</span></span>
<span data-ttu-id="92dbe-122">SyncGroup 輸入物件</span><span class="sxs-lookup"><span data-stu-id="92dbe-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92dbe-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="92dbe-123">-Name</span></span>
<span data-ttu-id="92dbe-124">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="92dbe-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92dbe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92dbe-125">-PassThru</span></span>
<span data-ttu-id="92dbe-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="92dbe-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="92dbe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92dbe-127">-ResourceGroupName</span></span>
<span data-ttu-id="92dbe-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="92dbe-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="92dbe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92dbe-129">-ResourceId</span></span>
<span data-ttu-id="92dbe-130">SyncGroup 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="92dbe-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="92dbe-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="92dbe-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="92dbe-132">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="92dbe-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92dbe-133">-確認</span><span class="sxs-lookup"><span data-stu-id="92dbe-133">-Confirm</span></span>
<span data-ttu-id="92dbe-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92dbe-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92dbe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92dbe-135">-WhatIf</span></span>
<span data-ttu-id="92dbe-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92dbe-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92dbe-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92dbe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92dbe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92dbe-138">CommonParameters</span></span>
<span data-ttu-id="92dbe-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92dbe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92dbe-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92dbe-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92dbe-141">輸入</span><span class="sxs-lookup"><span data-stu-id="92dbe-141">INPUTS</span></span>

### <span data-ttu-id="92dbe-142">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="92dbe-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="92dbe-143">System.object</span><span class="sxs-lookup"><span data-stu-id="92dbe-143">System.String</span></span>

### <span data-ttu-id="92dbe-144">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="92dbe-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92dbe-145">輸出</span><span class="sxs-lookup"><span data-stu-id="92dbe-145">OUTPUTS</span></span>

### <span data-ttu-id="92dbe-146">System.object</span><span class="sxs-lookup"><span data-stu-id="92dbe-146">System.Object</span></span>
## <span data-ttu-id="92dbe-147">筆記</span><span class="sxs-lookup"><span data-stu-id="92dbe-147">NOTES</span></span>

## <span data-ttu-id="92dbe-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="92dbe-148">RELATED LINKS</span></span>
