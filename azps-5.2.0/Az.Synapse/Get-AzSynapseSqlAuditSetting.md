---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281690"
---
# <span data-ttu-id="9e264-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="9e264-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="9e264-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e264-102">SYNOPSIS</span></span>
<span data-ttu-id="9e264-103">取得 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="9e264-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="9e264-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e264-104">SYNTAX</span></span>

### <span data-ttu-id="9e264-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9e264-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e264-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e264-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e264-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e264-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e264-108">說明</span><span class="sxs-lookup"><span data-stu-id="9e264-108">DESCRIPTION</span></span>
<span data-ttu-id="9e264-109">**AzSynapseSqlAuditSetting** Cmdlet 會取得 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="9e264-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="9e264-110">示例</span><span class="sxs-lookup"><span data-stu-id="9e264-110">EXAMPLES</span></span>

### <span data-ttu-id="9e264-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9e264-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9e264-112">取得名為 ContosoWorkspace 的工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="9e264-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9e264-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9e264-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="9e264-114">透過管道取得名為 ContosoWorkspace 的工作區審核設定。</span><span class="sxs-lookup"><span data-stu-id="9e264-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9e264-115">參數</span><span class="sxs-lookup"><span data-stu-id="9e264-115">PARAMETERS</span></span>

### <span data-ttu-id="9e264-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e264-116">-DefaultProfile</span></span>
<span data-ttu-id="9e264-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e264-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e264-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e264-118">-InputObject</span></span>
<span data-ttu-id="9e264-119">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="9e264-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e264-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e264-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e264-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9e264-121">Resource group name.</span></span>

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

### <span data-ttu-id="9e264-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e264-122">-ResourceId</span></span>
<span data-ttu-id="9e264-123">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e264-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e264-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e264-124">-WorkspaceName</span></span>
<span data-ttu-id="9e264-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e264-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e264-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e264-126">CommonParameters</span></span>
<span data-ttu-id="9e264-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e264-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e264-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e264-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e264-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9e264-129">INPUTS</span></span>

### <span data-ttu-id="9e264-130">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9e264-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9e264-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9e264-131">OUTPUTS</span></span>

### <span data-ttu-id="9e264-132">WorkspaceAuditModel 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9e264-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="9e264-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9e264-133">NOTES</span></span>

## <span data-ttu-id="9e264-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e264-134">RELATED LINKS</span></span>
