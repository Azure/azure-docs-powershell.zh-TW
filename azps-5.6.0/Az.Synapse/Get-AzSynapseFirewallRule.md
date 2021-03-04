---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 71622fbfa60a8961f10346aa9197b2c019f31bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909378"
---
# <span data-ttu-id="3cf8f-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3cf8f-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="3cf8f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3cf8f-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf8f-103">獲得 Synapse Analytics 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3cf8f-104">語法</span><span class="sxs-lookup"><span data-stu-id="3cf8f-104">SYNTAX</span></span>

### <span data-ttu-id="3cf8f-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3cf8f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cf8f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf8f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cf8f-107">描述</span><span class="sxs-lookup"><span data-stu-id="3cf8f-107">DESCRIPTION</span></span>
<span data-ttu-id="3cf8f-108">**Get-AzSynapseFirewallRule** Cmdlet 會取得 Azure Synapse Analytics Firewall Rule。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="3cf8f-109">如果您未指定規則名稱，此 Cmdlet 會獲得所有規則。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="3cf8f-110">例子</span><span class="sxs-lookup"><span data-stu-id="3cf8f-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf8f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3cf8f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3cf8f-112">此命令會獲得工作區下的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="3cf8f-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="3cf8f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="3cf8f-114">此命令會獲得工作區 ContosoWorkspace 下的防火牆規則，名稱為 ContosoFirewallRule。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="3cf8f-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="3cf8f-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="3cf8f-116">此命令會透過管線在工作區下獲得所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="3cf8f-117">參數</span><span class="sxs-lookup"><span data-stu-id="3cf8f-117">PARAMETERS</span></span>

### <span data-ttu-id="3cf8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf8f-118">-DefaultProfile</span></span>
<span data-ttu-id="3cf8f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf8f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cf8f-120">-Name</span></span>
<span data-ttu-id="3cf8f-121">工作區的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3cf8f-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-123">Resource group name.</span></span>

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

### <span data-ttu-id="3cf8f-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3cf8f-124">-WorkspaceName</span></span>
<span data-ttu-id="3cf8f-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3cf8f-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="3cf8f-126">-WorkSpaceObject</span></span>
<span data-ttu-id="3cf8f-127">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3cf8f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf8f-128">CommonParameters</span></span>
<span data-ttu-id="3cf8f-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3cf8f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf8f-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cf8f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf8f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3cf8f-131">INPUTS</span></span>

### <span data-ttu-id="3cf8f-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3cf8f-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3cf8f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3cf8f-133">OUTPUTS</span></span>

### <span data-ttu-id="3cf8f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3cf8f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="3cf8f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3cf8f-135">NOTES</span></span>

## <span data-ttu-id="3cf8f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cf8f-136">RELATED LINKS</span></span>
