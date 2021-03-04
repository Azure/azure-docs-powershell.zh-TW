---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ef4684cd6f4c852a9833dfdbe8c26ae1df6d326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902686"
---
# <span data-ttu-id="86247-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="86247-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="86247-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86247-102">SYNOPSIS</span></span>
<span data-ttu-id="86247-103">會取回可還原 Synapse Analytics SQL 資料庫的明顯還原點。</span><span class="sxs-lookup"><span data-stu-id="86247-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="86247-104">語法</span><span class="sxs-lookup"><span data-stu-id="86247-104">SYNTAX</span></span>

### <span data-ttu-id="86247-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="86247-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86247-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86247-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86247-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86247-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86247-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86247-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86247-109">描述</span><span class="sxs-lookup"><span data-stu-id="86247-109">DESCRIPTION</span></span>
<span data-ttu-id="86247-110">**Get-AzSynapseSqlPoolRestorePoint** Cmdlet 會從 Azure Synapse Analytics SQL 資料庫還原到不同的還原點。</span><span class="sxs-lookup"><span data-stu-id="86247-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="86247-111">例子</span><span class="sxs-lookup"><span data-stu-id="86247-111">EXAMPLES</span></span>

### <span data-ttu-id="86247-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="86247-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="86247-113">此命令會針對名為 ContosoSqlPool 的 Azure Synapse Analytics SQL Pool，會返回所有可用的還原點。</span><span class="sxs-lookup"><span data-stu-id="86247-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="86247-114">參數</span><span class="sxs-lookup"><span data-stu-id="86247-114">PARAMETERS</span></span>

### <span data-ttu-id="86247-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86247-115">-DefaultProfile</span></span>
<span data-ttu-id="86247-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="86247-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86247-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86247-117">-InputObject</span></span>
<span data-ttu-id="86247-118">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="86247-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86247-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="86247-119">-Name</span></span>
<span data-ttu-id="86247-120">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="86247-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86247-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86247-121">-ResourceGroupName</span></span>
<span data-ttu-id="86247-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="86247-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86247-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86247-123">-ResourceId</span></span>
<span data-ttu-id="86247-124">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="86247-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86247-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="86247-125">-WorkspaceName</span></span>
<span data-ttu-id="86247-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="86247-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86247-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="86247-127">-WorkspaceObject</span></span>
<span data-ttu-id="86247-128">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="86247-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86247-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86247-129">CommonParameters</span></span>
<span data-ttu-id="86247-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86247-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86247-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86247-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86247-132">輸入</span><span class="sxs-lookup"><span data-stu-id="86247-132">INPUTS</span></span>

### <span data-ttu-id="86247-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="86247-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="86247-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="86247-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="86247-135">輸出</span><span class="sxs-lookup"><span data-stu-id="86247-135">OUTPUTS</span></span>

### <span data-ttu-id="86247-136">Microsoft.Azure.management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="86247-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="86247-137">筆記</span><span class="sxs-lookup"><span data-stu-id="86247-137">NOTES</span></span>

## <span data-ttu-id="86247-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="86247-138">RELATED LINKS</span></span>
