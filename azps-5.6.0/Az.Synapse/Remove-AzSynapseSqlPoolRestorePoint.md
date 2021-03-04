---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906825"
---
# <span data-ttu-id="303d6-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="303d6-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="303d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="303d6-102">SYNOPSIS</span></span>
<span data-ttu-id="303d6-103">刪除 Synapse Analytics SQL 資料庫還原點。</span><span class="sxs-lookup"><span data-stu-id="303d6-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="303d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="303d6-104">SYNTAX</span></span>

### <span data-ttu-id="303d6-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="303d6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="303d6-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="303d6-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="303d6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="303d6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="303d6-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="303d6-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="303d6-109">描述</span><span class="sxs-lookup"><span data-stu-id="303d6-109">DESCRIPTION</span></span>
<span data-ttu-id="303d6-110">**Remove-AzSynapseSqlPoolRestorePoint** Cmdlet 會永久刪除 Azure Synapse Analytics SQL 資料庫還原點。</span><span class="sxs-lookup"><span data-stu-id="303d6-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="303d6-111">例子</span><span class="sxs-lookup"><span data-stu-id="303d6-111">EXAMPLES</span></span>

### <span data-ttu-id="303d6-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="303d6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="303d6-113">此命令會刪除 Azure Synapse Analytics SQL 資料庫還原點。</span><span class="sxs-lookup"><span data-stu-id="303d6-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="303d6-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="303d6-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="303d6-115">此命令會刪除透過管線的 Azure Synapse Analytics SQL 資料庫還原點。</span><span class="sxs-lookup"><span data-stu-id="303d6-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="303d6-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="303d6-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="303d6-117">此命令會刪除透過管線的 Azure Synapse Analytics SQL 資料庫還原點。</span><span class="sxs-lookup"><span data-stu-id="303d6-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="303d6-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="303d6-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="303d6-119">此命令會刪除具有指定資源識別碼的 Azure Synapse Analytics SQL 資料庫還原點。</span><span class="sxs-lookup"><span data-stu-id="303d6-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="303d6-120">參數</span><span class="sxs-lookup"><span data-stu-id="303d6-120">PARAMETERS</span></span>

### <span data-ttu-id="303d6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="303d6-121">-AsJob</span></span>
<span data-ttu-id="303d6-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="303d6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="303d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303d6-123">-DefaultProfile</span></span>
<span data-ttu-id="303d6-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="303d6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="303d6-125">-強制</span><span class="sxs-lookup"><span data-stu-id="303d6-125">-Force</span></span>
<span data-ttu-id="303d6-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="303d6-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="303d6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="303d6-127">-InputObject</span></span>
<span data-ttu-id="303d6-128">SQL 資料庫還原點建立時間輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="303d6-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="303d6-129">-Name</span></span>
<span data-ttu-id="303d6-130">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="303d6-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="303d6-131">-PassThru</span></span>
<span data-ttu-id="303d6-132">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="303d6-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="303d6-133">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="303d6-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="303d6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303d6-134">-ResourceGroupName</span></span>
<span data-ttu-id="303d6-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="303d6-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="303d6-136">-ResourceId</span></span>
<span data-ttu-id="303d6-137">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="303d6-137">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="303d6-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="303d6-139">Synapse SQL 還原點建立日期的名稱。</span><span class="sxs-lookup"><span data-stu-id="303d6-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="303d6-140">-SqlPoolObject</span></span>
<span data-ttu-id="303d6-141">Sql Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="303d6-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="303d6-142">-WorkspaceName</span></span>
<span data-ttu-id="303d6-143">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="303d6-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303d6-144">-確認</span><span class="sxs-lookup"><span data-stu-id="303d6-144">-Confirm</span></span>
<span data-ttu-id="303d6-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="303d6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303d6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303d6-146">-WhatIf</span></span>
<span data-ttu-id="303d6-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="303d6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="303d6-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="303d6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="303d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303d6-149">CommonParameters</span></span>
<span data-ttu-id="303d6-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="303d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303d6-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="303d6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303d6-152">輸入</span><span class="sxs-lookup"><span data-stu-id="303d6-152">INPUTS</span></span>

### <span data-ttu-id="303d6-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="303d6-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="303d6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="303d6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="303d6-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="303d6-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="303d6-156">System.String</span><span class="sxs-lookup"><span data-stu-id="303d6-156">System.String</span></span>

## <span data-ttu-id="303d6-157">輸出</span><span class="sxs-lookup"><span data-stu-id="303d6-157">OUTPUTS</span></span>

### <span data-ttu-id="303d6-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="303d6-158">System.Boolean</span></span>

## <span data-ttu-id="303d6-159">筆記</span><span class="sxs-lookup"><span data-stu-id="303d6-159">NOTES</span></span>

## <span data-ttu-id="303d6-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="303d6-160">RELATED LINKS</span></span>
