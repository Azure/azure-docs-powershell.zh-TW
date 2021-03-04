---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f35e4787779c49b399659f5e01ed8002df2e19ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917849"
---
# <span data-ttu-id="a168c-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a168c-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a168c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a168c-102">SYNOPSIS</span></span>
<span data-ttu-id="a168c-103">為工作區獲取進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="a168c-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="a168c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a168c-104">SYNTAX</span></span>

### <span data-ttu-id="a168c-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a168c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a168c-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a168c-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a168c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a168c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a168c-108">描述</span><span class="sxs-lookup"><span data-stu-id="a168c-108">DESCRIPTION</span></span>
<span data-ttu-id="a168c-109">**Get-AzSynapseSqlAdvancedThreatProtectionSetting** Cmdlet 取得 Azure Synapse Analytics Workspace 的進一代威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="a168c-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a168c-110">例子</span><span class="sxs-lookup"><span data-stu-id="a168c-110">EXAMPLES</span></span>

### <span data-ttu-id="a168c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a168c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a168c-112">此命令會針對名為 ContosoWorkspace 的工作區，獲得進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="a168c-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a168c-113">參數</span><span class="sxs-lookup"><span data-stu-id="a168c-113">PARAMETERS</span></span>

### <span data-ttu-id="a168c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a168c-114">-DefaultProfile</span></span>
<span data-ttu-id="a168c-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a168c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a168c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a168c-116">-InputObject</span></span>
<span data-ttu-id="a168c-117">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="a168c-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a168c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a168c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a168c-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a168c-119">Resource group name.</span></span>

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

### <span data-ttu-id="a168c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a168c-120">-ResourceId</span></span>
<span data-ttu-id="a168c-121">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a168c-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a168c-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a168c-122">-WorkspaceName</span></span>
<span data-ttu-id="a168c-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a168c-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a168c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a168c-124">CommonParameters</span></span>
<span data-ttu-id="a168c-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a168c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a168c-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a168c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a168c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a168c-127">INPUTS</span></span>

### <span data-ttu-id="a168c-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a168c-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a168c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a168c-129">OUTPUTS</span></span>

### <span data-ttu-id="a168c-130">Microsoft.Azure.Commands.Synapse.models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="a168c-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="a168c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a168c-131">NOTES</span></span>

## <span data-ttu-id="a168c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a168c-132">RELATED LINKS</span></span>
