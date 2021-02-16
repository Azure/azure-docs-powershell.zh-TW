---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139119"
---
# <span data-ttu-id="51a93-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="51a93-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="51a93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51a93-102">SYNOPSIS</span></span>
<span data-ttu-id="51a93-103">從目前的訂閱中移除指定的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="51a93-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="51a93-104">句法</span><span class="sxs-lookup"><span data-stu-id="51a93-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51a93-105">說明</span><span class="sxs-lookup"><span data-stu-id="51a93-105">DESCRIPTION</span></span>
<span data-ttu-id="51a93-106">**AzHDInsightCluster** Cmdlet 會將指定的 HDInsight 服務群集從訂閱中移除。</span><span class="sxs-lookup"><span data-stu-id="51a93-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="51a93-107">這個作業也會刪除任何儲存在 Hadoop 分散式檔案系統)  (在群集上的資料。</span><span class="sxs-lookup"><span data-stu-id="51a93-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="51a93-108">儲存在關聯之 Azure 儲存空間帳戶中的資料不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="51a93-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="51a93-109">儲存在外部 metastores 的資料不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="51a93-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="51a93-110">示例</span><span class="sxs-lookup"><span data-stu-id="51a93-110">EXAMPLES</span></span>

### <span data-ttu-id="51a93-111">範例1：刪除 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="51a93-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="51a93-112">這個命令會移除名為 [您的-hadoop-001] 的群集。</span><span class="sxs-lookup"><span data-stu-id="51a93-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="51a93-113">參數</span><span class="sxs-lookup"><span data-stu-id="51a93-113">PARAMETERS</span></span>

### <span data-ttu-id="51a93-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="51a93-114">-ClusterName</span></span>
<span data-ttu-id="51a93-115">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="51a93-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="51a93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a93-116">-DefaultProfile</span></span>
<span data-ttu-id="51a93-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="51a93-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51a93-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51a93-118">-PassThru</span></span>
<span data-ttu-id="51a93-119">如果 PassThru 都存在，則輸出結果</span><span class="sxs-lookup"><span data-stu-id="51a93-119">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="51a93-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a93-120">-ResourceGroupName</span></span>
<span data-ttu-id="51a93-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="51a93-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="51a93-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a93-122">CommonParameters</span></span>
<span data-ttu-id="51a93-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51a93-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a93-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="51a93-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a93-125">輸入</span><span class="sxs-lookup"><span data-stu-id="51a93-125">INPUTS</span></span>

### <span data-ttu-id="51a93-126">所有</span><span class="sxs-lookup"><span data-stu-id="51a93-126">None</span></span>
## <span data-ttu-id="51a93-127">輸出</span><span class="sxs-lookup"><span data-stu-id="51a93-127">OUTPUTS</span></span>

### <span data-ttu-id="51a93-128">System.object</span><span class="sxs-lookup"><span data-stu-id="51a93-128">System.Boolean</span></span>
## <span data-ttu-id="51a93-129">筆記</span><span class="sxs-lookup"><span data-stu-id="51a93-129">NOTES</span></span>

## <span data-ttu-id="51a93-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="51a93-130">RELATED LINKS</span></span>

[<span data-ttu-id="51a93-131">AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="51a93-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="51a93-132">使用-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="51a93-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


