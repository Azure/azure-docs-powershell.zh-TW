---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133430"
---
# <span data-ttu-id="67286-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="67286-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="67286-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67286-102">SYNOPSIS</span></span>
<span data-ttu-id="67286-103">這個命令會刪除指定的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="67286-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="67286-104">句法</span><span class="sxs-lookup"><span data-stu-id="67286-104">SYNTAX</span></span>

### <span data-ttu-id="67286-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="67286-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67286-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67286-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67286-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67286-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67286-108">說明</span><span class="sxs-lookup"><span data-stu-id="67286-108">DESCRIPTION</span></span>
<span data-ttu-id="67286-109">這個命令會刪除指定的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="67286-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="67286-110">只有在第一次刪除所有包含的端點時，才能移除同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="67286-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="67286-111">示例</span><span class="sxs-lookup"><span data-stu-id="67286-111">EXAMPLES</span></span>

### <span data-ttu-id="67286-112">範例1</span><span class="sxs-lookup"><span data-stu-id="67286-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="67286-113">這個命令會移除 [同步處理] 群組。</span><span class="sxs-lookup"><span data-stu-id="67286-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="67286-114">參數</span><span class="sxs-lookup"><span data-stu-id="67286-114">PARAMETERS</span></span>

### <span data-ttu-id="67286-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67286-115">-AsJob</span></span>
<span data-ttu-id="67286-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67286-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67286-117">-DefaultProfile</span></span>
<span data-ttu-id="67286-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67286-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67286-119">-Force</span><span class="sxs-lookup"><span data-stu-id="67286-119">-Force</span></span>
<span data-ttu-id="67286-120">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="67286-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="67286-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67286-121">-InputObject</span></span>
<span data-ttu-id="67286-122">SyncGroup 輸入物件</span><span class="sxs-lookup"><span data-stu-id="67286-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="67286-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="67286-123">-Name</span></span>
<span data-ttu-id="67286-124">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="67286-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="67286-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67286-125">-PassThru</span></span>
<span data-ttu-id="67286-126">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="67286-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="67286-127">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="67286-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="67286-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67286-128">-ResourceGroupName</span></span>
<span data-ttu-id="67286-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="67286-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="67286-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67286-130">-ResourceId</span></span>
<span data-ttu-id="67286-131">SyncGroup 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="67286-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="67286-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="67286-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="67286-133">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="67286-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="67286-134">-確認</span><span class="sxs-lookup"><span data-stu-id="67286-134">-Confirm</span></span>
<span data-ttu-id="67286-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67286-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67286-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67286-136">-WhatIf</span></span>
<span data-ttu-id="67286-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67286-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67286-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67286-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67286-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67286-139">CommonParameters</span></span>
<span data-ttu-id="67286-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67286-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67286-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67286-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67286-142">輸入</span><span class="sxs-lookup"><span data-stu-id="67286-142">INPUTS</span></span>

### <span data-ttu-id="67286-143">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="67286-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="67286-144">System.object</span><span class="sxs-lookup"><span data-stu-id="67286-144">System.String</span></span>

### <span data-ttu-id="67286-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="67286-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67286-146">輸出</span><span class="sxs-lookup"><span data-stu-id="67286-146">OUTPUTS</span></span>

### <span data-ttu-id="67286-147">System.object</span><span class="sxs-lookup"><span data-stu-id="67286-147">System.Object</span></span>
## <span data-ttu-id="67286-148">筆記</span><span class="sxs-lookup"><span data-stu-id="67286-148">NOTES</span></span>

## <span data-ttu-id="67286-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="67286-149">RELATED LINKS</span></span>
