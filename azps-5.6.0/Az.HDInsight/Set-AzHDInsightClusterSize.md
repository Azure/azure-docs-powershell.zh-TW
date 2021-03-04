---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: eba552917b17b9bb1337a2b62c83d3d1adebc1cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914834"
---
# <span data-ttu-id="6561c-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="6561c-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="6561c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6561c-102">SYNOPSIS</span></span>
<span data-ttu-id="6561c-103">設定指定組集中的工作者節點數目。</span><span class="sxs-lookup"><span data-stu-id="6561c-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="6561c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6561c-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6561c-105">描述</span><span class="sxs-lookup"><span data-stu-id="6561c-105">DESCRIPTION</span></span>
<span data-ttu-id="6561c-106">**Set-AzHDInsightClusterSize Cmdlet** 會設定指定 Azure HDInsight 叢集中的工作者節點數目。</span><span class="sxs-lookup"><span data-stu-id="6561c-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6561c-107">例子</span><span class="sxs-lookup"><span data-stu-id="6561c-107">EXAMPLES</span></span>

### <span data-ttu-id="6561c-108">範例 1：設定指定組的大小</span><span class="sxs-lookup"><span data-stu-id="6561c-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="6561c-109">此命令會設定名為 your-hadoop-001 的組的大小。</span><span class="sxs-lookup"><span data-stu-id="6561c-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6561c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6561c-110">PARAMETERS</span></span>

### <span data-ttu-id="6561c-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6561c-111">-ClusterName</span></span>
<span data-ttu-id="6561c-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="6561c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6561c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6561c-113">-DefaultProfile</span></span>
<span data-ttu-id="6561c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6561c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6561c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6561c-115">-ResourceGroupName</span></span>
<span data-ttu-id="6561c-116">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6561c-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6561c-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="6561c-117">-TargetInstanceCount</span></span>
<span data-ttu-id="6561c-118">指定在組集中需要的工作者節點數目。</span><span class="sxs-lookup"><span data-stu-id="6561c-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6561c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6561c-119">CommonParameters</span></span>
<span data-ttu-id="6561c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6561c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6561c-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6561c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6561c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6561c-122">INPUTS</span></span>

### <span data-ttu-id="6561c-123">沒有</span><span class="sxs-lookup"><span data-stu-id="6561c-123">None</span></span>

## <span data-ttu-id="6561c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6561c-124">OUTPUTS</span></span>

### <span data-ttu-id="6561c-125">Microsoft.Azure.management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="6561c-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="6561c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6561c-126">NOTES</span></span>

## <span data-ttu-id="6561c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6561c-127">RELATED LINKS</span></span>
