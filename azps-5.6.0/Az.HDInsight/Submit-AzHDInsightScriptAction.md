---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 9481c16db393a9147a4730b4c5f496e86c94eb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912390"
---
# <span data-ttu-id="e48c0-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e48c0-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="e48c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e48c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e48c0-103">將新的腳本動作提交至 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="e48c0-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e48c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="e48c0-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e48c0-105">描述</span><span class="sxs-lookup"><span data-stu-id="e48c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e48c0-106">**Submit-AzHDInsightScriptAction** Cmdlet 會提交新的腳本動作至 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="e48c0-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="e48c0-107">使用 *PersistOnSuccess* 讓腳本動作每次縮放時執行，只要腳本動作一開始成功。</span><span class="sxs-lookup"><span data-stu-id="e48c0-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="e48c0-108">例子</span><span class="sxs-lookup"><span data-stu-id="e48c0-108">EXAMPLES</span></span>

### <span data-ttu-id="e48c0-109">範例 1：提交新腳本動作至執行中的 HDInsight 集區</span><span class="sxs-lookup"><span data-stu-id="e48c0-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="e48c0-110">此命令會提交腳本動作至執行中的 HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="e48c0-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="e48c0-111">參數</span><span class="sxs-lookup"><span data-stu-id="e48c0-111">PARAMETERS</span></span>

### <span data-ttu-id="e48c0-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e48c0-112">-ApplicationName</span></span>
<span data-ttu-id="e48c0-113">指定腳本動作的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e48c0-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="e48c0-114">指定 *ApplicationName* 時 *，PersistOnSuccess 應該* 設定為 False，節點必須只包含 edgenode，而腳本動作計數應該等於 1。</span><span class="sxs-lookup"><span data-stu-id="e48c0-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="e48c0-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e48c0-115">-ClusterName</span></span>
<span data-ttu-id="e48c0-116">指定組名。</span><span class="sxs-lookup"><span data-stu-id="e48c0-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e48c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48c0-117">-DefaultProfile</span></span>
<span data-ttu-id="e48c0-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e48c0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e48c0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e48c0-119">-Name</span></span>
<span data-ttu-id="e48c0-120">指定腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e48c0-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="e48c0-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="e48c0-121">-NodeTypes</span></span>
<span data-ttu-id="e48c0-122">指定執行腳本動作的節點類型。</span><span class="sxs-lookup"><span data-stu-id="e48c0-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="e48c0-123">-參數</span><span class="sxs-lookup"><span data-stu-id="e48c0-123">-Parameters</span></span>
<span data-ttu-id="e48c0-124">指定腳本動作的參數。</span><span class="sxs-lookup"><span data-stu-id="e48c0-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="e48c0-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="e48c0-125">-PersistOnSuccess</span></span>
<span data-ttu-id="e48c0-126">表示每一次縮放該組組時，腳本動作應執行。</span><span class="sxs-lookup"><span data-stu-id="e48c0-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="e48c0-127">如果腳本動作一開始失敗，此參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e48c0-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="e48c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e48c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e48c0-129">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e48c0-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e48c0-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="e48c0-130">-Uri</span></span>
<span data-ttu-id="e48c0-131">指定 PowerShell 或 Bash 腳本 (腳本動作的公用 URI) 。</span><span class="sxs-lookup"><span data-stu-id="e48c0-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="e48c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48c0-132">CommonParameters</span></span>
<span data-ttu-id="e48c0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e48c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48c0-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e48c0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48c0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e48c0-135">INPUTS</span></span>

### <span data-ttu-id="e48c0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e48c0-136">System.String</span></span>

### <span data-ttu-id="e48c0-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="e48c0-137">System.Uri</span></span>

### <span data-ttu-id="e48c0-138">Microsoft.Azure.Commands.HDInsight.models.management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="e48c0-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="e48c0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e48c0-139">OUTPUTS</span></span>

### <span data-ttu-id="e48c0-140">Microsoft.Azure.Commands.HDInsight.models.management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="e48c0-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="e48c0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e48c0-141">NOTES</span></span>

## <span data-ttu-id="e48c0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e48c0-142">RELATED LINKS</span></span>

[<span data-ttu-id="e48c0-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e48c0-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


