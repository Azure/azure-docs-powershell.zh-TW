---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281685"
---
# <span data-ttu-id="5b28c-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="5b28c-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="5b28c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b28c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b28c-103">取得 Azure Synapse Analytics SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5b28c-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5b28c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b28c-104">SYNTAX</span></span>

### <span data-ttu-id="5b28c-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b28c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b28c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b28c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b28c-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b28c-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b28c-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b28c-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b28c-109">說明</span><span class="sxs-lookup"><span data-stu-id="5b28c-109">DESCRIPTION</span></span>
<span data-ttu-id="5b28c-110">**AzSynapseSqlPoolAuditSetting** Cmdlet 會取得 Azure SYNAPSE Analytics SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5b28c-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5b28c-111">示例</span><span class="sxs-lookup"><span data-stu-id="5b28c-111">EXAMPLES</span></span>

### <span data-ttu-id="5b28c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="5b28c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="5b28c-113">這個命令會在工作區 ContosoWorkspace 中取得名為 ContosoSqlPool 之 SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5b28c-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5b28c-114">範例2</span><span class="sxs-lookup"><span data-stu-id="5b28c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="5b28c-115">這個命令會透過管線在工作區 ContosoWorkspace 中取得名為 ContosoSqlPool 的 SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5b28c-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5b28c-116">參數</span><span class="sxs-lookup"><span data-stu-id="5b28c-116">PARAMETERS</span></span>

### <span data-ttu-id="5b28c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b28c-117">-DefaultProfile</span></span>
<span data-ttu-id="5b28c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b28c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b28c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b28c-119">-InputObject</span></span>
<span data-ttu-id="5b28c-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5b28c-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5b28c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b28c-121">-Name</span></span>
<span data-ttu-id="5b28c-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b28c-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5b28c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b28c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b28c-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5b28c-124">Resource group name.</span></span>

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

### <span data-ttu-id="5b28c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b28c-125">-ResourceId</span></span>
<span data-ttu-id="5b28c-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b28c-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="5b28c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b28c-127">-WorkspaceName</span></span>
<span data-ttu-id="5b28c-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b28c-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5b28c-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5b28c-129">-WorkspaceObject</span></span>
<span data-ttu-id="5b28c-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5b28c-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5b28c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b28c-131">CommonParameters</span></span>
<span data-ttu-id="5b28c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b28c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b28c-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b28c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b28c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5b28c-134">INPUTS</span></span>

### <span data-ttu-id="5b28c-135">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5b28c-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5b28c-136">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5b28c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5b28c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5b28c-137">OUTPUTS</span></span>

### <span data-ttu-id="5b28c-138">SqlPoolAuditModel 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5b28c-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="5b28c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5b28c-139">NOTES</span></span>

## <span data-ttu-id="5b28c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b28c-140">RELATED LINKS</span></span>
