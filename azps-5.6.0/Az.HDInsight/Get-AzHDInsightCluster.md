---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: c89293ee071aba3fcec2d58d071714193cc44a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916736"
---
# <span data-ttu-id="c66a7-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c66a7-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="c66a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c66a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c66a7-103">獲取並列出與目前訂閱或指定資源群組相關聯的所有 Azure HDInsight 群組，或取回特定的群組。</span><span class="sxs-lookup"><span data-stu-id="c66a7-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="c66a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="c66a7-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c66a7-105">描述</span><span class="sxs-lookup"><span data-stu-id="c66a7-105">DESCRIPTION</span></span>
<span data-ttu-id="c66a7-106">**Get-AzHDInsightCluster Cmdlet** 會列出目前訂閱的 Azure HDInsight 服務叢集。</span><span class="sxs-lookup"><span data-stu-id="c66a7-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="c66a7-107">使用 *ClusterName* 參數取得特定組的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c66a7-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="c66a7-108">例子</span><span class="sxs-lookup"><span data-stu-id="c66a7-108">EXAMPLES</span></span>

### <span data-ttu-id="c66a7-109">範例 1：列出所有 Azure HDInsight 集區</span><span class="sxs-lookup"><span data-stu-id="c66a7-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="c66a7-110">此命令會列出所有 Azure HDInsight 的集區。</span><span class="sxs-lookup"><span data-stu-id="c66a7-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="c66a7-111">參數</span><span class="sxs-lookup"><span data-stu-id="c66a7-111">PARAMETERS</span></span>

### <span data-ttu-id="c66a7-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c66a7-112">-ClusterName</span></span>
<span data-ttu-id="c66a7-113">指定組名。</span><span class="sxs-lookup"><span data-stu-id="c66a7-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66a7-114">-DefaultProfile</span></span>
<span data-ttu-id="c66a7-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c66a7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c66a7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c66a7-116">-ResourceGroupName</span></span>
<span data-ttu-id="c66a7-117">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c66a7-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66a7-118">CommonParameters</span></span>
<span data-ttu-id="c66a7-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c66a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66a7-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c66a7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66a7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c66a7-121">INPUTS</span></span>

### <span data-ttu-id="c66a7-122">沒有</span><span class="sxs-lookup"><span data-stu-id="c66a7-122">None</span></span>

## <span data-ttu-id="c66a7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c66a7-123">OUTPUTS</span></span>

### <span data-ttu-id="c66a7-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c66a7-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c66a7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c66a7-125">NOTES</span></span>

## <span data-ttu-id="c66a7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c66a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="c66a7-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c66a7-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="c66a7-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c66a7-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


