---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: a14079c92a59864b98dd086d8e65a340e2a277d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912185"
---
# <span data-ttu-id="f2307-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="f2307-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="f2307-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2307-102">SYNOPSIS</span></span>
<span data-ttu-id="f2307-103">取消 Synapse Analytics Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="f2307-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f2307-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2307-104">SYNTAX</span></span>

### <span data-ttu-id="f2307-105">StopSparkStatementByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2307-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2307-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2307-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2307-107">描述</span><span class="sxs-lookup"><span data-stu-id="f2307-107">DESCRIPTION</span></span>
<span data-ttu-id="f2307-108">**Stop-AzSynapseSparkStatement Cmdlet** 會取消 Synapse Analytics Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="f2307-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f2307-109">例子</span><span class="sxs-lookup"><span data-stu-id="f2307-109">EXAMPLES</span></span>

### <span data-ttu-id="f2307-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2307-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="f2307-111">此命令會取消具有指定 利維識別碼的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="f2307-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="f2307-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="f2307-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="f2307-113">此命令會透過管線取消具有指定 利忘識別碼的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="f2307-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="f2307-114">參數</span><span class="sxs-lookup"><span data-stu-id="f2307-114">PARAMETERS</span></span>

### <span data-ttu-id="f2307-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2307-115">-DefaultProfile</span></span>
<span data-ttu-id="f2307-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2307-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2307-117">-強制</span><span class="sxs-lookup"><span data-stu-id="f2307-117">-Force</span></span>
<span data-ttu-id="f2307-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="f2307-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2307-119">-利維Id</span><span class="sxs-lookup"><span data-stu-id="f2307-119">-LivyId</span></span>
<span data-ttu-id="f2307-120">Spark 語句的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2307-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="f2307-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2307-121">-PassThru</span></span>
<span data-ttu-id="f2307-122">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="f2307-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f2307-123">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="f2307-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f2307-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="f2307-124">-SessionId</span></span>
<span data-ttu-id="f2307-125">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2307-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="f2307-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="f2307-126">-SessionObject</span></span>
<span data-ttu-id="f2307-127">Spark 會話輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="f2307-127">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f2307-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f2307-128">-SparkPoolName</span></span>
<span data-ttu-id="f2307-129">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2307-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f2307-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f2307-130">-WorkspaceName</span></span>
<span data-ttu-id="f2307-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2307-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f2307-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f2307-132">-Confirm</span></span>
<span data-ttu-id="f2307-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f2307-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2307-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2307-134">-WhatIf</span></span>
<span data-ttu-id="f2307-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2307-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2307-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2307-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2307-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2307-137">CommonParameters</span></span>
<span data-ttu-id="f2307-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2307-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2307-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2307-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2307-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f2307-140">INPUTS</span></span>

### <span data-ttu-id="f2307-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f2307-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f2307-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f2307-142">OUTPUTS</span></span>

### <span data-ttu-id="f2307-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2307-143">System.Boolean</span></span>

## <span data-ttu-id="f2307-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f2307-144">NOTES</span></span>

## <span data-ttu-id="f2307-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2307-145">RELATED LINKS</span></span>
