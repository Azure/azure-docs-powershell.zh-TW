---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: 38c6d45c4e49f86d3aacc2774942d15ddd50941e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907433"
---
# <span data-ttu-id="2f0ed-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f0ed-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="2f0ed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0ed-103">此命令將會刪除指定的同步組。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="2f0ed-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f0ed-104">SYNTAX</span></span>

### <span data-ttu-id="2f0ed-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2f0ed-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ed-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f0ed-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f0ed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f0ed-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0ed-108">描述</span><span class="sxs-lookup"><span data-stu-id="2f0ed-108">DESCRIPTION</span></span>
<span data-ttu-id="2f0ed-109">此命令將會刪除指定的同步組。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="2f0ed-110">只有先刪除所有包含的端點時，才能移除同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="2f0ed-111">例子</span><span class="sxs-lookup"><span data-stu-id="2f0ed-111">EXAMPLES</span></span>

### <span data-ttu-id="2f0ed-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f0ed-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="2f0ed-113">此命令會移除同步群組。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="2f0ed-114">參數</span><span class="sxs-lookup"><span data-stu-id="2f0ed-114">PARAMETERS</span></span>

### <span data-ttu-id="2f0ed-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f0ed-115">-AsJob</span></span>
<span data-ttu-id="2f0ed-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f0ed-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f0ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0ed-117">-DefaultProfile</span></span>
<span data-ttu-id="2f0ed-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f0ed-119">-強制</span><span class="sxs-lookup"><span data-stu-id="2f0ed-119">-Force</span></span>
<span data-ttu-id="2f0ed-120">提供 -強制跳過此命令的確認。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="2f0ed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f0ed-121">-InputObject</span></span>
<span data-ttu-id="2f0ed-122">SyncGroup 輸入物件</span><span class="sxs-lookup"><span data-stu-id="2f0ed-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="2f0ed-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f0ed-123">-Name</span></span>
<span data-ttu-id="2f0ed-124">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="2f0ed-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f0ed-125">-PassThru</span></span>
<span data-ttu-id="2f0ed-126">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="2f0ed-127">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="2f0ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f0ed-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="2f0ed-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0ed-130">-ResourceId</span></span>
<span data-ttu-id="2f0ed-131">SyncGroup 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2f0ed-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="2f0ed-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2f0ed-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="2f0ed-133">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="2f0ed-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2f0ed-134">-Confirm</span></span>
<span data-ttu-id="2f0ed-135">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0ed-136">-WhatIf</span></span>
<span data-ttu-id="2f0ed-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f0ed-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0ed-139">CommonParameters</span></span>
<span data-ttu-id="2f0ed-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0ed-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2f0ed-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0ed-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2f0ed-142">INPUTS</span></span>

### <span data-ttu-id="2f0ed-143">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f0ed-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="2f0ed-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2f0ed-144">System.String</span></span>

### <span data-ttu-id="2f0ed-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f0ed-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f0ed-146">輸出</span><span class="sxs-lookup"><span data-stu-id="2f0ed-146">OUTPUTS</span></span>

### <span data-ttu-id="2f0ed-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="2f0ed-147">System.Object</span></span>
## <span data-ttu-id="2f0ed-148">筆記</span><span class="sxs-lookup"><span data-stu-id="2f0ed-148">NOTES</span></span>

## <span data-ttu-id="2f0ed-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f0ed-149">RELATED LINKS</span></span>
