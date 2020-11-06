---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 76cf830e79c2374d81c57a1341ae99636333e273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450612"
---
# <span data-ttu-id="c545d-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c545d-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="c545d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c545d-102">SYNOPSIS</span></span>
<span data-ttu-id="c545d-103">取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。</span><span class="sxs-lookup"><span data-stu-id="c545d-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c545d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c545d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c545d-105">說明</span><span class="sxs-lookup"><span data-stu-id="c545d-105">DESCRIPTION</span></span>
<span data-ttu-id="c545d-106">**AzureRmHDInsightCluster** Cmdlet 會列出目前訂閱的 Azure HDInsight 服務群集。</span><span class="sxs-lookup"><span data-stu-id="c545d-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="c545d-107">使用 *ClusterName* 參數來取得特定群集的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c545d-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="c545d-108">示例</span><span class="sxs-lookup"><span data-stu-id="c545d-108">EXAMPLES</span></span>

### <span data-ttu-id="c545d-109">範例1：列出所有 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="c545d-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="c545d-110">這個命令會列出所有的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="c545d-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="c545d-111">參數</span><span class="sxs-lookup"><span data-stu-id="c545d-111">PARAMETERS</span></span>

### <span data-ttu-id="c545d-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c545d-112">-ClusterName</span></span>
<span data-ttu-id="c545d-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c545d-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c545d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c545d-114">-DefaultProfile</span></span>
<span data-ttu-id="c545d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c545d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c545d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c545d-116">-ResourceGroupName</span></span>
<span data-ttu-id="c545d-117">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c545d-117">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c545d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c545d-118">CommonParameters</span></span>
<span data-ttu-id="c545d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c545d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c545d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c545d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c545d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c545d-121">INPUTS</span></span>

### <span data-ttu-id="c545d-122">所有</span><span class="sxs-lookup"><span data-stu-id="c545d-122">None</span></span>
<span data-ttu-id="c545d-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c545d-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c545d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c545d-124">OUTPUTS</span></span>

### <span data-ttu-id="c545d-125">[System.object]。清單 ' 1 [AzureHDInsightCluster] （）</span><span class="sxs-lookup"><span data-stu-id="c545d-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="c545d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c545d-126">NOTES</span></span>

## <span data-ttu-id="c545d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c545d-127">RELATED LINKS</span></span>

[<span data-ttu-id="c545d-128">移除-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c545d-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="c545d-129">使用-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c545d-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


