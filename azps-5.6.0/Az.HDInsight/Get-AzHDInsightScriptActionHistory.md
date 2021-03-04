---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 8273ad77091d008bead41e568f6c9d2de0e0d6f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909702"
---
# <span data-ttu-id="8aafa-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="8aafa-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="8aafa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8aafa-102">SYNOPSIS</span></span>
<span data-ttu-id="8aafa-103">獲得該組群的腳本動作歷程記錄，並以反向時間順序列出，或獲得先前執行的腳本動作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8aafa-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="8aafa-104">語法</span><span class="sxs-lookup"><span data-stu-id="8aafa-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aafa-105">描述</span><span class="sxs-lookup"><span data-stu-id="8aafa-105">DESCRIPTION</span></span>
<span data-ttu-id="8aafa-106">**Get-AzHDInsightScriptActionHistory Cmdlet** 會取得 Azure HDInsight 集區腳本動作歷程記錄，並按相反的時間順序列出，或取得先前執行的腳本動作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8aafa-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="8aafa-107">例子</span><span class="sxs-lookup"><span data-stu-id="8aafa-107">EXAMPLES</span></span>

### <span data-ttu-id="8aafa-108">範例 1：取得該組組腳本動作執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="8aafa-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="8aafa-109">此命令會獲得您-hadoop-001 該組組腳本動作的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="8aafa-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="8aafa-110">參數</span><span class="sxs-lookup"><span data-stu-id="8aafa-110">PARAMETERS</span></span>

### <span data-ttu-id="8aafa-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8aafa-111">-ClusterName</span></span>
<span data-ttu-id="8aafa-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="8aafa-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8aafa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aafa-113">-DefaultProfile</span></span>
<span data-ttu-id="8aafa-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8aafa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aafa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aafa-115">-ResourceGroupName</span></span>
<span data-ttu-id="8aafa-116">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aafa-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8aafa-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="8aafa-117">-ScriptExecutionId</span></span>
<span data-ttu-id="8aafa-118">指定執行腳本動作的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="8aafa-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aafa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aafa-119">CommonParameters</span></span>
<span data-ttu-id="8aafa-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8aafa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aafa-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aafa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aafa-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8aafa-122">INPUTS</span></span>

### <span data-ttu-id="8aafa-123">沒有</span><span class="sxs-lookup"><span data-stu-id="8aafa-123">None</span></span>

## <span data-ttu-id="8aafa-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8aafa-124">OUTPUTS</span></span>

### <span data-ttu-id="8aafa-125">Microsoft.Azure.Commands.HDInsight.models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="8aafa-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="8aafa-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8aafa-126">NOTES</span></span>

## <span data-ttu-id="8aafa-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8aafa-127">RELATED LINKS</span></span>
