---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137195"
---
# <span data-ttu-id="0da76-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0da76-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="0da76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0da76-102">SYNOPSIS</span></span>
<span data-ttu-id="0da76-103">檢索可還原 Synapse Analytics SQL pool 的不同還原點。</span><span class="sxs-lookup"><span data-stu-id="0da76-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="0da76-104">句法</span><span class="sxs-lookup"><span data-stu-id="0da76-104">SYNTAX</span></span>

### <span data-ttu-id="0da76-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0da76-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da76-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da76-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da76-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da76-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0da76-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da76-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0da76-109">說明</span><span class="sxs-lookup"><span data-stu-id="0da76-109">DESCRIPTION</span></span>
<span data-ttu-id="0da76-110">**AzSynapseSqlPoolRestorePoint** Cmdlet 會檢索 Azure SYNAPSE Analytics SQL pool 可以還原的不同還原點。</span><span class="sxs-lookup"><span data-stu-id="0da76-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="0da76-111">示例</span><span class="sxs-lookup"><span data-stu-id="0da76-111">EXAMPLES</span></span>

### <span data-ttu-id="0da76-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0da76-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="0da76-113">這個命令會傳回 Azure Synapse Analytics SQL pool （名為 ContosoSqlPool）的所有可用還原點。</span><span class="sxs-lookup"><span data-stu-id="0da76-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="0da76-114">參數</span><span class="sxs-lookup"><span data-stu-id="0da76-114">PARAMETERS</span></span>

### <span data-ttu-id="0da76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da76-115">-DefaultProfile</span></span>
<span data-ttu-id="0da76-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0da76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da76-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0da76-117">-InputObject</span></span>
<span data-ttu-id="0da76-118">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0da76-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0da76-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0da76-119">-Name</span></span>
<span data-ttu-id="0da76-120">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0da76-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0da76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da76-121">-ResourceGroupName</span></span>
<span data-ttu-id="0da76-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0da76-122">Resource group name.</span></span>

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

### <span data-ttu-id="0da76-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0da76-123">-ResourceId</span></span>
<span data-ttu-id="0da76-124">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0da76-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="0da76-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0da76-125">-WorkspaceName</span></span>
<span data-ttu-id="0da76-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0da76-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0da76-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0da76-127">-WorkspaceObject</span></span>
<span data-ttu-id="0da76-128">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0da76-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0da76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da76-129">CommonParameters</span></span>
<span data-ttu-id="0da76-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0da76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da76-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0da76-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da76-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0da76-132">INPUTS</span></span>

### <span data-ttu-id="0da76-133">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0da76-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0da76-134">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0da76-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0da76-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0da76-135">OUTPUTS</span></span>

### <span data-ttu-id="0da76-136">RestorePoint 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0da76-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="0da76-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0da76-137">NOTES</span></span>

## <span data-ttu-id="0da76-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0da76-138">RELATED LINKS</span></span>
