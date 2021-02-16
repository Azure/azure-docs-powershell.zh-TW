---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137678"
---
# <span data-ttu-id="7a627-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7a627-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="7a627-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a627-102">SYNOPSIS</span></span>
<span data-ttu-id="7a627-103">修改 SQL pool 的 TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="7a627-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="7a627-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a627-104">SYNTAX</span></span>

### <span data-ttu-id="7a627-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7a627-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a627-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a627-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a627-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a627-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a627-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a627-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a627-109">說明</span><span class="sxs-lookup"><span data-stu-id="7a627-109">DESCRIPTION</span></span>
<span data-ttu-id="7a627-110">**AzSynapseSqlPoolTransparentDataEncryption** Cmdlet 會修改) Azure SYNAPSE Analytics SQL Pool 的透明資料加密 (TDE 屬性。</span><span class="sxs-lookup"><span data-stu-id="7a627-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7a627-111">示例</span><span class="sxs-lookup"><span data-stu-id="7a627-111">EXAMPLES</span></span>

### <span data-ttu-id="7a627-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7a627-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="7a627-113">這個命令會在名為 ContosoWorkspace 的工作區下，為名為 ContosoSqlPool 的 SQL pool 啟用 TDE。</span><span class="sxs-lookup"><span data-stu-id="7a627-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7a627-114">參數</span><span class="sxs-lookup"><span data-stu-id="7a627-114">PARAMETERS</span></span>

### <span data-ttu-id="7a627-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a627-115">-AsJob</span></span>
<span data-ttu-id="7a627-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a627-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a627-117">-DefaultProfile</span></span>
<span data-ttu-id="7a627-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a627-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a627-119">-InputObject</span></span>
<span data-ttu-id="7a627-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="7a627-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7a627-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a627-121">-Name</span></span>
<span data-ttu-id="7a627-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a627-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="7a627-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a627-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a627-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7a627-124">Resource group name.</span></span>

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

### <span data-ttu-id="7a627-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a627-125">-ResourceId</span></span>
<span data-ttu-id="7a627-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a627-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="7a627-127">-State</span><span class="sxs-lookup"><span data-stu-id="7a627-127">-State</span></span>
<span data-ttu-id="7a627-128">Azure Synapse Analytics Sql Pool 透明資料加密狀態。</span><span class="sxs-lookup"><span data-stu-id="7a627-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="7a627-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a627-129">-WorkspaceName</span></span>
<span data-ttu-id="7a627-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a627-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7a627-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7a627-131">-WorkspaceObject</span></span>
<span data-ttu-id="7a627-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="7a627-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7a627-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7a627-133">-Confirm</span></span>
<span data-ttu-id="7a627-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7a627-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a627-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a627-135">-WhatIf</span></span>
<span data-ttu-id="7a627-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a627-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a627-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a627-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a627-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a627-138">CommonParameters</span></span>
<span data-ttu-id="7a627-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a627-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a627-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7a627-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a627-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7a627-141">INPUTS</span></span>

### <span data-ttu-id="7a627-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7a627-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7a627-143">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7a627-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7a627-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7a627-144">OUTPUTS</span></span>

### <span data-ttu-id="7a627-145">PSTransparentDataEncryption 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7a627-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="7a627-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7a627-146">NOTES</span></span>

## <span data-ttu-id="7a627-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a627-147">RELATED LINKS</span></span>
