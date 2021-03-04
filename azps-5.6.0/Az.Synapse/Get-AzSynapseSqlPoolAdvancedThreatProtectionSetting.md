---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c706de537f4d95603399540342bd3ad52d2b30fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917841"
---
# <span data-ttu-id="24a55-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="24a55-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="24a55-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24a55-102">SYNOPSIS</span></span>
<span data-ttu-id="24a55-103">為 SQL 資料庫獲取進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="24a55-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="24a55-104">語法</span><span class="sxs-lookup"><span data-stu-id="24a55-104">SYNTAX</span></span>

### <span data-ttu-id="24a55-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24a55-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a55-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24a55-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a55-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24a55-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a55-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24a55-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24a55-109">描述</span><span class="sxs-lookup"><span data-stu-id="24a55-109">DESCRIPTION</span></span>
<span data-ttu-id="24a55-110">**Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** Cmdlet 取得 Azure Synapse Analytics SQL 資料庫的進一代威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="24a55-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="24a55-111">例子</span><span class="sxs-lookup"><span data-stu-id="24a55-111">EXAMPLES</span></span>

### <span data-ttu-id="24a55-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="24a55-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="24a55-113">此命令會針對名為 ContosoWorkspace 的工作區下名為 ContosoSqlPool 的 SQL 資料庫，獲得進一步的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="24a55-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="24a55-114">參數</span><span class="sxs-lookup"><span data-stu-id="24a55-114">PARAMETERS</span></span>

### <span data-ttu-id="24a55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a55-115">-DefaultProfile</span></span>
<span data-ttu-id="24a55-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24a55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a55-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24a55-117">-InputObject</span></span>
<span data-ttu-id="24a55-118">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="24a55-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="24a55-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="24a55-119">-Name</span></span>
<span data-ttu-id="24a55-120">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="24a55-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="24a55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a55-121">-ResourceGroupName</span></span>
<span data-ttu-id="24a55-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="24a55-122">Resource group name.</span></span>

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

### <span data-ttu-id="24a55-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a55-123">-ResourceId</span></span>
<span data-ttu-id="24a55-124">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24a55-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="24a55-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24a55-125">-WorkspaceName</span></span>
<span data-ttu-id="24a55-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="24a55-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="24a55-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="24a55-127">-WorkspaceObject</span></span>
<span data-ttu-id="24a55-128">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="24a55-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="24a55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a55-129">CommonParameters</span></span>
<span data-ttu-id="24a55-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24a55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a55-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24a55-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a55-132">輸入</span><span class="sxs-lookup"><span data-stu-id="24a55-132">INPUTS</span></span>

### <span data-ttu-id="24a55-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24a55-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="24a55-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="24a55-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="24a55-135">輸出</span><span class="sxs-lookup"><span data-stu-id="24a55-135">OUTPUTS</span></span>

### <span data-ttu-id="24a55-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="24a55-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="24a55-137">筆記</span><span class="sxs-lookup"><span data-stu-id="24a55-137">NOTES</span></span>

## <span data-ttu-id="24a55-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="24a55-138">RELATED LINKS</span></span>
