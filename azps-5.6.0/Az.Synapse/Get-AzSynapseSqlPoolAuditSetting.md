---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: dea94d89bfd5384d8ec614259a5bb342cd9d186b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917834"
---
# <span data-ttu-id="309a6-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="309a6-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="309a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="309a6-102">SYNOPSIS</span></span>
<span data-ttu-id="309a6-103">獲得 Azure Synapse Analytics SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="309a6-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="309a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="309a6-104">SYNTAX</span></span>

### <span data-ttu-id="309a6-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="309a6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="309a6-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="309a6-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="309a6-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="309a6-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="309a6-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="309a6-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="309a6-109">描述</span><span class="sxs-lookup"><span data-stu-id="309a6-109">DESCRIPTION</span></span>
<span data-ttu-id="309a6-110">**Get-AzSynapseSqlPoolAuditSetting** Cmdlet 會取得 Azure Synapse Analytics SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="309a6-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="309a6-111">例子</span><span class="sxs-lookup"><span data-stu-id="309a6-111">EXAMPLES</span></span>

### <span data-ttu-id="309a6-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="309a6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="309a6-113">此命令會獲得工作區 ContosoWorkspace 中稱為 ContosoSqlPool 的 SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="309a6-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="309a6-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="309a6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="309a6-115">此命令會透過管線在工作區 ContosoWorkspace 中，獲得稱為 ContosoSqlPool 的 SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="309a6-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="309a6-116">參數</span><span class="sxs-lookup"><span data-stu-id="309a6-116">PARAMETERS</span></span>

### <span data-ttu-id="309a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309a6-117">-DefaultProfile</span></span>
<span data-ttu-id="309a6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="309a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="309a6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="309a6-119">-InputObject</span></span>
<span data-ttu-id="309a6-120">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="309a6-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="309a6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="309a6-121">-Name</span></span>
<span data-ttu-id="309a6-122">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="309a6-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="309a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="309a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="309a6-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="309a6-124">Resource group name.</span></span>

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

### <span data-ttu-id="309a6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="309a6-125">-ResourceId</span></span>
<span data-ttu-id="309a6-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="309a6-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="309a6-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="309a6-127">-WorkspaceName</span></span>
<span data-ttu-id="309a6-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="309a6-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="309a6-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="309a6-129">-WorkspaceObject</span></span>
<span data-ttu-id="309a6-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="309a6-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="309a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309a6-131">CommonParameters</span></span>
<span data-ttu-id="309a6-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="309a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309a6-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="309a6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309a6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="309a6-134">INPUTS</span></span>

### <span data-ttu-id="309a6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="309a6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="309a6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="309a6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="309a6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="309a6-137">OUTPUTS</span></span>

### <span data-ttu-id="309a6-138">Microsoft.Azure.Commands.Synapse.models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="309a6-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="309a6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="309a6-139">NOTES</span></span>

## <span data-ttu-id="309a6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="309a6-140">RELATED LINKS</span></span>
