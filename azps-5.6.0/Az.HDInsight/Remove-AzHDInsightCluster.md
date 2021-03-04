---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: 5baf67bfec2c4e18e718241dbb973bb8b2050bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905397"
---
# <span data-ttu-id="d985a-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d985a-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="d985a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d985a-102">SYNOPSIS</span></span>
<span data-ttu-id="d985a-103">從目前的訂閱移除指定的 HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="d985a-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="d985a-104">語法</span><span class="sxs-lookup"><span data-stu-id="d985a-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d985a-105">描述</span><span class="sxs-lookup"><span data-stu-id="d985a-105">DESCRIPTION</span></span>
<span data-ttu-id="d985a-106">**Remove-AzHDInsightCluster Cmdlet** 會從訂閱移除指定的 HDInsight 服務叢集。</span><span class="sxs-lookup"><span data-stu-id="d985a-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="d985a-107">這項作業也會刪除儲存在 Hadoop 分散式檔案系統中 (HDFS) 組上的任何資料。</span><span class="sxs-lookup"><span data-stu-id="d985a-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="d985a-108">不會刪除儲存在相關聯 Azure 儲存體帳戶中的資料。</span><span class="sxs-lookup"><span data-stu-id="d985a-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="d985a-109">不會刪除儲存在外部元存放區的資料。</span><span class="sxs-lookup"><span data-stu-id="d985a-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="d985a-110">例子</span><span class="sxs-lookup"><span data-stu-id="d985a-110">EXAMPLES</span></span>

### <span data-ttu-id="d985a-111">範例 1：刪除 Azure HDInsight 集區</span><span class="sxs-lookup"><span data-stu-id="d985a-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="d985a-112">此命令會移除名為 your-hadoop-001 的組。</span><span class="sxs-lookup"><span data-stu-id="d985a-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d985a-113">參數</span><span class="sxs-lookup"><span data-stu-id="d985a-113">PARAMETERS</span></span>

### <span data-ttu-id="d985a-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d985a-114">-ClusterName</span></span>
<span data-ttu-id="d985a-115">指定組名。</span><span class="sxs-lookup"><span data-stu-id="d985a-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d985a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d985a-116">-DefaultProfile</span></span>
<span data-ttu-id="d985a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d985a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d985a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d985a-118">-PassThru</span></span>
<span data-ttu-id="d985a-119">如果 PassThru 存在，則輸出結果</span><span class="sxs-lookup"><span data-stu-id="d985a-119">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="d985a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d985a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d985a-121">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d985a-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d985a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d985a-122">CommonParameters</span></span>
<span data-ttu-id="d985a-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d985a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d985a-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d985a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d985a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d985a-125">INPUTS</span></span>

### <span data-ttu-id="d985a-126">沒有</span><span class="sxs-lookup"><span data-stu-id="d985a-126">None</span></span>
## <span data-ttu-id="d985a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="d985a-127">OUTPUTS</span></span>

### <span data-ttu-id="d985a-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d985a-128">System.Boolean</span></span>
## <span data-ttu-id="d985a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d985a-129">NOTES</span></span>

## <span data-ttu-id="d985a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d985a-130">RELATED LINKS</span></span>

[<span data-ttu-id="d985a-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d985a-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="d985a-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d985a-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


