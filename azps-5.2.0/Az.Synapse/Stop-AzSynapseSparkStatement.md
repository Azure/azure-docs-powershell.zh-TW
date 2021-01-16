---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279746"
---
# <span data-ttu-id="864d0-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="864d0-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="864d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="864d0-102">SYNOPSIS</span></span>
<span data-ttu-id="864d0-103">取消 Synapse 分析 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="864d0-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="864d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="864d0-104">SYNTAX</span></span>

### <span data-ttu-id="864d0-105">StopSparkStatementByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="864d0-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="864d0-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="864d0-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864d0-107">說明</span><span class="sxs-lookup"><span data-stu-id="864d0-107">DESCRIPTION</span></span>
<span data-ttu-id="864d0-108">**AzSynapseSparkStatement** Cmdlet 會取消 Synapse 分析 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="864d0-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="864d0-109">示例</span><span class="sxs-lookup"><span data-stu-id="864d0-109">EXAMPLES</span></span>

### <span data-ttu-id="864d0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="864d0-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="864d0-111">這個命令會取消具有指定 livy 識別碼的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="864d0-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="864d0-112">範例2</span><span class="sxs-lookup"><span data-stu-id="864d0-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="864d0-113">這個命令會透過管線取消具有指定 livy ID 的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="864d0-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="864d0-114">參數</span><span class="sxs-lookup"><span data-stu-id="864d0-114">PARAMETERS</span></span>

### <span data-ttu-id="864d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864d0-115">-DefaultProfile</span></span>
<span data-ttu-id="864d0-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="864d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="864d0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="864d0-117">-Force</span></span>
<span data-ttu-id="864d0-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="864d0-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="864d0-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="864d0-119">-LivyId</span></span>
<span data-ttu-id="864d0-120">Spark 語句的識別碼。</span><span class="sxs-lookup"><span data-stu-id="864d0-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864d0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="864d0-121">-PassThru</span></span>
<span data-ttu-id="864d0-122">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="864d0-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="864d0-123">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="864d0-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="864d0-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="864d0-124">-SessionId</span></span>
<span data-ttu-id="864d0-125">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="864d0-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864d0-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="864d0-126">-SessionObject</span></span>
<span data-ttu-id="864d0-127">觸發會話輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="864d0-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="864d0-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="864d0-128">-SparkPoolName</span></span>
<span data-ttu-id="864d0-129">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="864d0-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864d0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="864d0-130">-WorkspaceName</span></span>
<span data-ttu-id="864d0-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="864d0-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864d0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="864d0-132">-Confirm</span></span>
<span data-ttu-id="864d0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="864d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="864d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864d0-134">-WhatIf</span></span>
<span data-ttu-id="864d0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="864d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="864d0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="864d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864d0-137">CommonParameters</span></span>
<span data-ttu-id="864d0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="864d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864d0-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="864d0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864d0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="864d0-140">INPUTS</span></span>

### <span data-ttu-id="864d0-141">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="864d0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="864d0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="864d0-142">OUTPUTS</span></span>

### <span data-ttu-id="864d0-143">System.object</span><span class="sxs-lookup"><span data-stu-id="864d0-143">System.Boolean</span></span>

## <span data-ttu-id="864d0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="864d0-144">NOTES</span></span>

## <span data-ttu-id="864d0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="864d0-145">RELATED LINKS</span></span>
