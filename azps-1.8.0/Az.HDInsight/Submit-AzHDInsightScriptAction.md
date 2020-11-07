---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: ef1c06c475b5de4984abf7859f033d68ad7d9dfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787614"
---
# <span data-ttu-id="272bf-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="272bf-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="272bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="272bf-102">SYNOPSIS</span></span>
<span data-ttu-id="272bf-103">將新的腳本指令提交至 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="272bf-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="272bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="272bf-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="272bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="272bf-105">DESCRIPTION</span></span>
<span data-ttu-id="272bf-106">**Submit AzHDInsightScriptAction** Cmdlet 會將新的腳本指令提交至 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="272bf-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="272bf-107">只要腳本動作最初成功，就可以使用 *PersistOnSuccess* 在每次群集放大時執行腳本動作。</span><span class="sxs-lookup"><span data-stu-id="272bf-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="272bf-108">示例</span><span class="sxs-lookup"><span data-stu-id="272bf-108">EXAMPLES</span></span>

### <span data-ttu-id="272bf-109">範例1：提交新的腳本指令至正在執行的 HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="272bf-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="272bf-110">這個命令會將腳本動作提交至正在執行的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="272bf-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="272bf-111">參數</span><span class="sxs-lookup"><span data-stu-id="272bf-111">PARAMETERS</span></span>

### <span data-ttu-id="272bf-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="272bf-112">-ApplicationName</span></span>
<span data-ttu-id="272bf-113">指定腳本動作的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="272bf-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="272bf-114">指定 *ApplicationName* 之後， *PersistOnSuccess* 應該設定為 False，節點只能包含 edgenode，而腳本動作計數應該等於1。</span><span class="sxs-lookup"><span data-stu-id="272bf-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="272bf-115">-ClusterName</span></span>
<span data-ttu-id="272bf-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="272bf-116">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272bf-117">-DefaultProfile</span></span>
<span data-ttu-id="272bf-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="272bf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="272bf-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="272bf-119">-Name</span></span>
<span data-ttu-id="272bf-120">指定腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="272bf-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="272bf-121">-NodeTypes</span></span>
<span data-ttu-id="272bf-122">指定要在其上執行腳本動作的節點類型。</span><span class="sxs-lookup"><span data-stu-id="272bf-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-123">-參數</span><span class="sxs-lookup"><span data-stu-id="272bf-123">-Parameters</span></span>
<span data-ttu-id="272bf-124">指定腳本動作的參數。</span><span class="sxs-lookup"><span data-stu-id="272bf-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="272bf-125">-PersistOnSuccess</span></span>
<span data-ttu-id="272bf-126">表示每當群集放大時，腳本動作應該會執行。</span><span class="sxs-lookup"><span data-stu-id="272bf-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="272bf-127">如果腳本動作最初失敗，則會略過這個切換參數。</span><span class="sxs-lookup"><span data-stu-id="272bf-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272bf-128">-ResourceGroupName</span></span>
<span data-ttu-id="272bf-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="272bf-129">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="272bf-130">-Uri</span></span>
<span data-ttu-id="272bf-131">指定 PowerShell 或 Bash 腳本)  (腳本操作的公用 URI。</span><span class="sxs-lookup"><span data-stu-id="272bf-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272bf-132">CommonParameters</span></span>
<span data-ttu-id="272bf-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="272bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272bf-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="272bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272bf-135">輸入</span><span class="sxs-lookup"><span data-stu-id="272bf-135">INPUTS</span></span>

### <span data-ttu-id="272bf-136">System.object</span><span class="sxs-lookup"><span data-stu-id="272bf-136">System.String</span></span>

### <span data-ttu-id="272bf-137">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="272bf-137">System.Uri</span></span>

### <span data-ttu-id="272bf-138">RuntimeScriptActionClusterNodeType [] （[]）</span><span class="sxs-lookup"><span data-stu-id="272bf-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="272bf-139">輸出</span><span class="sxs-lookup"><span data-stu-id="272bf-139">OUTPUTS</span></span>

### <span data-ttu-id="272bf-140">AzureHDInsightRuntimeScriptActionOperationResource 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="272bf-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="272bf-141">筆記</span><span class="sxs-lookup"><span data-stu-id="272bf-141">NOTES</span></span>

## <span data-ttu-id="272bf-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="272bf-142">RELATED LINKS</span></span>

[<span data-ttu-id="272bf-143">附加 AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="272bf-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


