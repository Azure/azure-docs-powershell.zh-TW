---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 2a66333f5372308c87462f5ef9b2f7f5bfa8dd79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787701"
---
# <span data-ttu-id="13635-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="13635-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="13635-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13635-102">SYNOPSIS</span></span>
<span data-ttu-id="13635-103">取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="13635-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="13635-104">句法</span><span class="sxs-lookup"><span data-stu-id="13635-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13635-105">說明</span><span class="sxs-lookup"><span data-stu-id="13635-105">DESCRIPTION</span></span>
<span data-ttu-id="13635-106">**AzHDInsightScriptActionHistory** Cmdlet 會取得 Azure HDInsight 群集的腳本動作歷程記錄，並以相反的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="13635-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="13635-107">示例</span><span class="sxs-lookup"><span data-stu-id="13635-107">EXAMPLES</span></span>

### <span data-ttu-id="13635-108">範例1：取得群集的腳本動作執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="13635-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="13635-109">這個命令會針對您的 hadoop-001 取得群集的腳本動作歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="13635-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="13635-110">參數</span><span class="sxs-lookup"><span data-stu-id="13635-110">PARAMETERS</span></span>

### <span data-ttu-id="13635-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="13635-111">-ClusterName</span></span>
<span data-ttu-id="13635-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="13635-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="13635-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13635-113">-DefaultProfile</span></span>
<span data-ttu-id="13635-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13635-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13635-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13635-115">-ResourceGroupName</span></span>
<span data-ttu-id="13635-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13635-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="13635-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="13635-117">-ScriptExecutionId</span></span>
<span data-ttu-id="13635-118">指定執行的腳本動作的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="13635-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="13635-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13635-119">CommonParameters</span></span>
<span data-ttu-id="13635-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13635-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13635-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13635-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13635-122">輸入</span><span class="sxs-lookup"><span data-stu-id="13635-122">INPUTS</span></span>

### <span data-ttu-id="13635-123">所有</span><span class="sxs-lookup"><span data-stu-id="13635-123">None</span></span>

## <span data-ttu-id="13635-124">輸出</span><span class="sxs-lookup"><span data-stu-id="13635-124">OUTPUTS</span></span>

### <span data-ttu-id="13635-125">AzureHDInsightRuntimeScriptActionDetail 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="13635-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="13635-126">筆記</span><span class="sxs-lookup"><span data-stu-id="13635-126">NOTES</span></span>

## <span data-ttu-id="13635-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="13635-127">RELATED LINKS</span></span>