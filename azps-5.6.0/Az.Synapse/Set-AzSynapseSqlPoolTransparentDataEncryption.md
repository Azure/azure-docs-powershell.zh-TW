---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cdc72a2bb0e21873bd0fa2d82123afe8ed011378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912221"
---
# <span data-ttu-id="2d67a-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="2d67a-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="2d67a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d67a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d67a-103">修改 SQL 資料庫的 TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="2d67a-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="2d67a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d67a-104">SYNTAX</span></span>

### <span data-ttu-id="2d67a-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2d67a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d67a-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d67a-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d67a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d67a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d67a-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d67a-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d67a-109">描述</span><span class="sxs-lookup"><span data-stu-id="2d67a-109">DESCRIPTION</span></span>
<span data-ttu-id="2d67a-110">**Set-AzSynapseSqlPoolTransparentDataEncryption** Cmdlet 會修改 Azure Synapse Analytics SQL 集區中的透明資料加密 (TDE) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2d67a-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2d67a-111">例子</span><span class="sxs-lookup"><span data-stu-id="2d67a-111">EXAMPLES</span></span>

### <span data-ttu-id="2d67a-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2d67a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="2d67a-113">此命令會針對名為 ContosoWorkspace 的工作區下名為 ContosoSqlPool 的 SQL 資料庫啟用 TDE。</span><span class="sxs-lookup"><span data-stu-id="2d67a-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2d67a-114">參數</span><span class="sxs-lookup"><span data-stu-id="2d67a-114">PARAMETERS</span></span>

### <span data-ttu-id="2d67a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d67a-115">-AsJob</span></span>
<span data-ttu-id="2d67a-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d67a-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d67a-117">-DefaultProfile</span></span>
<span data-ttu-id="2d67a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d67a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d67a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d67a-119">-InputObject</span></span>
<span data-ttu-id="2d67a-120">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="2d67a-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d67a-121">-Name</span></span>
<span data-ttu-id="2d67a-122">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d67a-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d67a-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d67a-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2d67a-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d67a-125">-ResourceId</span></span>
<span data-ttu-id="2d67a-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d67a-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-127">-State</span><span class="sxs-lookup"><span data-stu-id="2d67a-127">-State</span></span>
<span data-ttu-id="2d67a-128">Azure Synapse Analytics Sql Pool 透明資料加密狀態。</span><span class="sxs-lookup"><span data-stu-id="2d67a-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d67a-129">-WorkspaceName</span></span>
<span data-ttu-id="2d67a-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d67a-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d67a-131">-WorkspaceObject</span></span>
<span data-ttu-id="2d67a-132">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="2d67a-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2d67a-133">-Confirm</span></span>
<span data-ttu-id="2d67a-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2d67a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d67a-135">-WhatIf</span></span>
<span data-ttu-id="2d67a-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d67a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d67a-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d67a-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d67a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d67a-138">CommonParameters</span></span>
<span data-ttu-id="2d67a-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d67a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d67a-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d67a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d67a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2d67a-141">INPUTS</span></span>

### <span data-ttu-id="2d67a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d67a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2d67a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2d67a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2d67a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2d67a-144">OUTPUTS</span></span>

### <span data-ttu-id="2d67a-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="2d67a-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="2d67a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2d67a-146">NOTES</span></span>

## <span data-ttu-id="2d67a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d67a-147">RELATED LINKS</span></span>
