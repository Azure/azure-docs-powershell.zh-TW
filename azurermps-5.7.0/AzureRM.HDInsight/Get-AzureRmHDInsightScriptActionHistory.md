---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: b2e302f9490cb5671728a46105ad574b54270c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444540"
---
# <span data-ttu-id="36541-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="36541-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="36541-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36541-102">SYNOPSIS</span></span>
<span data-ttu-id="36541-103">取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36541-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36541-104">句法</span><span class="sxs-lookup"><span data-stu-id="36541-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36541-105">說明</span><span class="sxs-lookup"><span data-stu-id="36541-105">DESCRIPTION</span></span>
<span data-ttu-id="36541-106">**AzureRmHDInsightScriptActionHistory** Cmdlet 會取得 Azure HDInsight 群集的腳本動作歷程記錄，並以相反的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36541-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="36541-107">示例</span><span class="sxs-lookup"><span data-stu-id="36541-107">EXAMPLES</span></span>

### <span data-ttu-id="36541-108">範例1：取得群集的腳本動作執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="36541-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="36541-109">這個命令會針對您的 hadoop-001 取得群集的腳本動作歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="36541-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="36541-110">參數</span><span class="sxs-lookup"><span data-stu-id="36541-110">PARAMETERS</span></span>

### <span data-ttu-id="36541-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="36541-111">-ClusterName</span></span>
<span data-ttu-id="36541-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="36541-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36541-113">-DefaultProfile</span></span>
<span data-ttu-id="36541-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="36541-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36541-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36541-115">-ResourceGroupName</span></span>
<span data-ttu-id="36541-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36541-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36541-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="36541-117">-ScriptExecutionId</span></span>
<span data-ttu-id="36541-118">指定執行的腳本動作的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="36541-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36541-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36541-119">CommonParameters</span></span>
<span data-ttu-id="36541-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36541-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36541-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36541-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36541-122">輸入</span><span class="sxs-lookup"><span data-stu-id="36541-122">INPUTS</span></span>

### <span data-ttu-id="36541-123">所有</span><span class="sxs-lookup"><span data-stu-id="36541-123">None</span></span>
<span data-ttu-id="36541-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="36541-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36541-125">輸出</span><span class="sxs-lookup"><span data-stu-id="36541-125">OUTPUTS</span></span>

### <span data-ttu-id="36541-126">System.object IList ' 1 [AzureHDInsightRuntimeScriptActionDetail] （即 Azure. 命令..]</span><span class="sxs-lookup"><span data-stu-id="36541-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="36541-127">筆記</span><span class="sxs-lookup"><span data-stu-id="36541-127">NOTES</span></span>

## <span data-ttu-id="36541-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="36541-128">RELATED LINKS</span></span>
