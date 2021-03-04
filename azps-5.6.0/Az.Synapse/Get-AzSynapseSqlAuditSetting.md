---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: cf32bea3942c89b408592778657e5ecffae2acd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917846"
---
# <span data-ttu-id="732ac-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="732ac-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="732ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="732ac-102">SYNOPSIS</span></span>
<span data-ttu-id="732ac-103">獲得 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="732ac-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="732ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="732ac-104">SYNTAX</span></span>

### <span data-ttu-id="732ac-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="732ac-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732ac-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="732ac-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="732ac-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="732ac-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="732ac-108">描述</span><span class="sxs-lookup"><span data-stu-id="732ac-108">DESCRIPTION</span></span>
<span data-ttu-id="732ac-109">**Get-AzSynapseSqlAuditSetting** Cmdlet 會取得 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="732ac-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="732ac-110">例子</span><span class="sxs-lookup"><span data-stu-id="732ac-110">EXAMPLES</span></span>

### <span data-ttu-id="732ac-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="732ac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="732ac-112">獲得名為 ContosoWorkspace 之工作區的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="732ac-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="732ac-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="732ac-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="732ac-114">透過管道，獲得名為 ContosoWorkspace 的工作區的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="732ac-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="732ac-115">參數</span><span class="sxs-lookup"><span data-stu-id="732ac-115">PARAMETERS</span></span>

### <span data-ttu-id="732ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732ac-116">-DefaultProfile</span></span>
<span data-ttu-id="732ac-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="732ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732ac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="732ac-118">-InputObject</span></span>
<span data-ttu-id="732ac-119">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="732ac-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="732ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="732ac-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="732ac-121">Resource group name.</span></span>

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

### <span data-ttu-id="732ac-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="732ac-122">-ResourceId</span></span>
<span data-ttu-id="732ac-123">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="732ac-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="732ac-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="732ac-124">-WorkspaceName</span></span>
<span data-ttu-id="732ac-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="732ac-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="732ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732ac-126">CommonParameters</span></span>
<span data-ttu-id="732ac-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="732ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732ac-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="732ac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732ac-129">輸入</span><span class="sxs-lookup"><span data-stu-id="732ac-129">INPUTS</span></span>

### <span data-ttu-id="732ac-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="732ac-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="732ac-131">輸出</span><span class="sxs-lookup"><span data-stu-id="732ac-131">OUTPUTS</span></span>

### <span data-ttu-id="732ac-132">Microsoft.Azure.Commands.Synapse.models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="732ac-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="732ac-133">筆記</span><span class="sxs-lookup"><span data-stu-id="732ac-133">NOTES</span></span>

## <span data-ttu-id="732ac-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="732ac-134">RELATED LINKS</span></span>
