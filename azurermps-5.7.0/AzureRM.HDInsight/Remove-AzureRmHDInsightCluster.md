---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: 1029871a2125668c732f7ff541582f06dbd790c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624501"
---
# <span data-ttu-id="59b5d-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59b5d-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="59b5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="59b5d-103">從目前的訂閱中移除指定的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="59b5d-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="59b5d-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b5d-105">說明</span><span class="sxs-lookup"><span data-stu-id="59b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="59b5d-106">**AzureRmHDInsightCluster** Cmdlet 會將指定的 HDInsight 服務群集從訂閱中移除。</span><span class="sxs-lookup"><span data-stu-id="59b5d-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="59b5d-107">這個作業也會刪除任何儲存在 Hadoop 分散式檔案系統)  (在群集上的資料。</span><span class="sxs-lookup"><span data-stu-id="59b5d-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="59b5d-108">儲存在關聯之 Azure 儲存空間帳戶中的資料不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="59b5d-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="59b5d-109">儲存在外部 metastores 的資料不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="59b5d-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="59b5d-110">示例</span><span class="sxs-lookup"><span data-stu-id="59b5d-110">EXAMPLES</span></span>

### <span data-ttu-id="59b5d-111">範例1：刪除 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="59b5d-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="59b5d-112">這個命令會移除名為 [您的-hadoop-001] 的群集。</span><span class="sxs-lookup"><span data-stu-id="59b5d-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="59b5d-113">參數</span><span class="sxs-lookup"><span data-stu-id="59b5d-113">PARAMETERS</span></span>

### <span data-ttu-id="59b5d-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="59b5d-114">-ClusterName</span></span>
<span data-ttu-id="59b5d-115">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="59b5d-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="59b5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b5d-116">-DefaultProfile</span></span>
<span data-ttu-id="59b5d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="59b5d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59b5d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b5d-118">-ResourceGroupName</span></span>
<span data-ttu-id="59b5d-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59b5d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="59b5d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b5d-120">CommonParameters</span></span>
<span data-ttu-id="59b5d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59b5d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b5d-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59b5d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b5d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="59b5d-123">INPUTS</span></span>

### <span data-ttu-id="59b5d-124">所有</span><span class="sxs-lookup"><span data-stu-id="59b5d-124">None</span></span>
<span data-ttu-id="59b5d-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="59b5d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59b5d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="59b5d-126">OUTPUTS</span></span>

### <span data-ttu-id="59b5d-127">ClusterGetResponse 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="59b5d-127">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="59b5d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="59b5d-128">NOTES</span></span>

## <span data-ttu-id="59b5d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="59b5d-129">RELATED LINKS</span></span>

[<span data-ttu-id="59b5d-130">AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59b5d-130">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="59b5d-131">使用-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59b5d-131">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


