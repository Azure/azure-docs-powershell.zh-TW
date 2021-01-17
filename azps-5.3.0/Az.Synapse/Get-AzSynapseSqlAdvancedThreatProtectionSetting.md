---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288275"
---
# <span data-ttu-id="67383-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="67383-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="67383-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67383-102">SYNOPSIS</span></span>
<span data-ttu-id="67383-103">取得工作區的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="67383-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="67383-104">句法</span><span class="sxs-lookup"><span data-stu-id="67383-104">SYNTAX</span></span>

### <span data-ttu-id="67383-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="67383-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67383-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67383-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67383-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67383-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67383-108">說明</span><span class="sxs-lookup"><span data-stu-id="67383-108">DESCRIPTION</span></span>
<span data-ttu-id="67383-109">**AzSynapseSqlAdvancedThreatProtectionSetting** Cmdlet 會取得 Azure Synapse Analytics 工作區的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="67383-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="67383-110">示例</span><span class="sxs-lookup"><span data-stu-id="67383-110">EXAMPLES</span></span>

### <span data-ttu-id="67383-111">範例1</span><span class="sxs-lookup"><span data-stu-id="67383-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="67383-112">這個命令會取得名為 ContosoWorkspace 之工作區的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="67383-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="67383-113">參數</span><span class="sxs-lookup"><span data-stu-id="67383-113">PARAMETERS</span></span>

### <span data-ttu-id="67383-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67383-114">-DefaultProfile</span></span>
<span data-ttu-id="67383-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67383-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67383-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67383-116">-InputObject</span></span>
<span data-ttu-id="67383-117">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="67383-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="67383-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67383-118">-ResourceGroupName</span></span>
<span data-ttu-id="67383-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="67383-119">Resource group name.</span></span>

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

### <span data-ttu-id="67383-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67383-120">-ResourceId</span></span>
<span data-ttu-id="67383-121">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="67383-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="67383-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67383-122">-WorkspaceName</span></span>
<span data-ttu-id="67383-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="67383-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="67383-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67383-124">CommonParameters</span></span>
<span data-ttu-id="67383-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67383-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67383-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67383-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67383-127">輸入</span><span class="sxs-lookup"><span data-stu-id="67383-127">INPUTS</span></span>

### <span data-ttu-id="67383-128">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="67383-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="67383-129">輸出</span><span class="sxs-lookup"><span data-stu-id="67383-129">OUTPUTS</span></span>

### <span data-ttu-id="67383-130">PSServerSecurityAlertPolicy 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="67383-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="67383-131">筆記</span><span class="sxs-lookup"><span data-stu-id="67383-131">NOTES</span></span>

## <span data-ttu-id="67383-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="67383-132">RELATED LINKS</span></span>
