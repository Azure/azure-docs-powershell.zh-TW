---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797714"
---
# <span data-ttu-id="895ae-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="895ae-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="895ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="895ae-102">SYNOPSIS</span></span>
<span data-ttu-id="895ae-103">設定指定群集中的工作人員節點數。</span><span class="sxs-lookup"><span data-stu-id="895ae-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="895ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="895ae-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="895ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="895ae-105">DESCRIPTION</span></span>
<span data-ttu-id="895ae-106">**AzHDInsightClusterSize** Cmdlet 會設定指定 Azure HDInsight 群集中的 Worker 節點數目。</span><span class="sxs-lookup"><span data-stu-id="895ae-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="895ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="895ae-107">EXAMPLES</span></span>

### <span data-ttu-id="895ae-108">範例1：設定指定群集的大小</span><span class="sxs-lookup"><span data-stu-id="895ae-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="895ae-109">這個命令會設定名為 [您的 hadoop-001] 的群集大小。</span><span class="sxs-lookup"><span data-stu-id="895ae-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="895ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="895ae-110">PARAMETERS</span></span>

### <span data-ttu-id="895ae-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="895ae-111">-ClusterName</span></span>
<span data-ttu-id="895ae-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="895ae-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="895ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895ae-113">-DefaultProfile</span></span>
<span data-ttu-id="895ae-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="895ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="895ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="895ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="895ae-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="895ae-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="895ae-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="895ae-117">-TargetInstanceCount</span></span>
<span data-ttu-id="895ae-118">指定群集中所需的輔助角色節點數目。</span><span class="sxs-lookup"><span data-stu-id="895ae-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="895ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895ae-119">CommonParameters</span></span>
<span data-ttu-id="895ae-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="895ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895ae-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="895ae-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895ae-122">輸入</span><span class="sxs-lookup"><span data-stu-id="895ae-122">INPUTS</span></span>

### <span data-ttu-id="895ae-123">所有</span><span class="sxs-lookup"><span data-stu-id="895ae-123">None</span></span>

## <span data-ttu-id="895ae-124">輸出</span><span class="sxs-lookup"><span data-stu-id="895ae-124">OUTPUTS</span></span>

### <span data-ttu-id="895ae-125">[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="895ae-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="895ae-126">筆記</span><span class="sxs-lookup"><span data-stu-id="895ae-126">NOTES</span></span>

## <span data-ttu-id="895ae-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="895ae-127">RELATED LINKS</span></span>