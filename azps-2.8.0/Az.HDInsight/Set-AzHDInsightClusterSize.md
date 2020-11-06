---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 1616714879a260dea3611809b5f7028b4a203d34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612270"
---
# <span data-ttu-id="8415f-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="8415f-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="8415f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8415f-102">SYNOPSIS</span></span>
<span data-ttu-id="8415f-103">設定指定群集中的工作人員節點數。</span><span class="sxs-lookup"><span data-stu-id="8415f-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="8415f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8415f-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8415f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8415f-105">DESCRIPTION</span></span>
<span data-ttu-id="8415f-106">**AzHDInsightClusterSize** Cmdlet 會設定指定 Azure HDInsight 群集中的 Worker 節點數目。</span><span class="sxs-lookup"><span data-stu-id="8415f-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8415f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8415f-107">EXAMPLES</span></span>

### <span data-ttu-id="8415f-108">範例1：設定指定群集的大小</span><span class="sxs-lookup"><span data-stu-id="8415f-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="8415f-109">這個命令會設定名為 [您的 hadoop-001] 的群集大小。</span><span class="sxs-lookup"><span data-stu-id="8415f-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8415f-110">參數</span><span class="sxs-lookup"><span data-stu-id="8415f-110">PARAMETERS</span></span>

### <span data-ttu-id="8415f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8415f-111">-ClusterName</span></span>
<span data-ttu-id="8415f-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8415f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8415f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8415f-113">-DefaultProfile</span></span>
<span data-ttu-id="8415f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8415f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8415f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8415f-115">-ResourceGroupName</span></span>
<span data-ttu-id="8415f-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8415f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8415f-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="8415f-117">-TargetInstanceCount</span></span>
<span data-ttu-id="8415f-118">指定群集中所需的輔助角色節點數目。</span><span class="sxs-lookup"><span data-stu-id="8415f-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="8415f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8415f-119">CommonParameters</span></span>
<span data-ttu-id="8415f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8415f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8415f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8415f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8415f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8415f-122">INPUTS</span></span>

### <span data-ttu-id="8415f-123">所有</span><span class="sxs-lookup"><span data-stu-id="8415f-123">None</span></span>

## <span data-ttu-id="8415f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8415f-124">OUTPUTS</span></span>

### <span data-ttu-id="8415f-125">[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="8415f-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="8415f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8415f-126">NOTES</span></span>

## <span data-ttu-id="8415f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8415f-127">RELATED LINKS</span></span>