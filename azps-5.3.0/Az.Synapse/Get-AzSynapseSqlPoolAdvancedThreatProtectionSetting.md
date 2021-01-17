---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288260"
---
# <span data-ttu-id="acc68-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="acc68-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="acc68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acc68-102">SYNOPSIS</span></span>
<span data-ttu-id="acc68-103">取得 SQL pool 的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="acc68-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="acc68-104">句法</span><span class="sxs-lookup"><span data-stu-id="acc68-104">SYNTAX</span></span>

### <span data-ttu-id="acc68-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="acc68-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc68-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc68-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc68-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc68-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc68-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc68-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc68-109">說明</span><span class="sxs-lookup"><span data-stu-id="acc68-109">DESCRIPTION</span></span>
<span data-ttu-id="acc68-110">**AzSynapseSqlPoolAdvancedThreatProtectionSetting** Cmdlet 會取得 Azure SYNAPSE Analytics SQL pool 的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="acc68-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="acc68-111">示例</span><span class="sxs-lookup"><span data-stu-id="acc68-111">EXAMPLES</span></span>

### <span data-ttu-id="acc68-112">範例1</span><span class="sxs-lookup"><span data-stu-id="acc68-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="acc68-113">這個命令會在名為 ContosoWorkspace 的工作區下，取得名為 ContosoSqlPool 之 SQL pool 的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="acc68-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="acc68-114">參數</span><span class="sxs-lookup"><span data-stu-id="acc68-114">PARAMETERS</span></span>

### <span data-ttu-id="acc68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc68-115">-DefaultProfile</span></span>
<span data-ttu-id="acc68-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acc68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc68-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acc68-117">-InputObject</span></span>
<span data-ttu-id="acc68-118">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="acc68-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="acc68-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="acc68-119">-Name</span></span>
<span data-ttu-id="acc68-120">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="acc68-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="acc68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc68-121">-ResourceGroupName</span></span>
<span data-ttu-id="acc68-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="acc68-122">Resource group name.</span></span>

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

### <span data-ttu-id="acc68-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acc68-123">-ResourceId</span></span>
<span data-ttu-id="acc68-124">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="acc68-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="acc68-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="acc68-125">-WorkspaceName</span></span>
<span data-ttu-id="acc68-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="acc68-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="acc68-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="acc68-127">-WorkspaceObject</span></span>
<span data-ttu-id="acc68-128">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="acc68-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="acc68-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc68-129">CommonParameters</span></span>
<span data-ttu-id="acc68-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acc68-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc68-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="acc68-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc68-132">輸入</span><span class="sxs-lookup"><span data-stu-id="acc68-132">INPUTS</span></span>

### <span data-ttu-id="acc68-133">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="acc68-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="acc68-134">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="acc68-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="acc68-135">輸出</span><span class="sxs-lookup"><span data-stu-id="acc68-135">OUTPUTS</span></span>

### <span data-ttu-id="acc68-136">PSSqlPoolSecurityAlertPolicy 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="acc68-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="acc68-137">筆記</span><span class="sxs-lookup"><span data-stu-id="acc68-137">NOTES</span></span>

## <span data-ttu-id="acc68-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="acc68-138">RELATED LINKS</span></span>
