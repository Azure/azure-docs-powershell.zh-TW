---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969540"
---
# <span data-ttu-id="cda94-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cda94-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="cda94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cda94-102">SYNOPSIS</span></span>
<span data-ttu-id="cda94-103">取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。</span><span class="sxs-lookup"><span data-stu-id="cda94-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="cda94-104">句法</span><span class="sxs-lookup"><span data-stu-id="cda94-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cda94-105">說明</span><span class="sxs-lookup"><span data-stu-id="cda94-105">DESCRIPTION</span></span>
<span data-ttu-id="cda94-106">**AzHDInsightCluster** Cmdlet 會列出目前訂閱的 Azure HDInsight 服務群集。</span><span class="sxs-lookup"><span data-stu-id="cda94-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="cda94-107">使用 *ClusterName* 參數來取得特定群集的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cda94-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="cda94-108">示例</span><span class="sxs-lookup"><span data-stu-id="cda94-108">EXAMPLES</span></span>

### <span data-ttu-id="cda94-109">範例1：列出所有 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="cda94-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="cda94-110">這個命令會列出所有的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="cda94-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="cda94-111">參數</span><span class="sxs-lookup"><span data-stu-id="cda94-111">PARAMETERS</span></span>

### <span data-ttu-id="cda94-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cda94-112">-ClusterName</span></span>
<span data-ttu-id="cda94-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="cda94-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cda94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda94-114">-DefaultProfile</span></span>
<span data-ttu-id="cda94-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cda94-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cda94-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda94-116">-ResourceGroupName</span></span>
<span data-ttu-id="cda94-117">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cda94-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cda94-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda94-118">CommonParameters</span></span>
<span data-ttu-id="cda94-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cda94-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda94-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cda94-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda94-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cda94-121">INPUTS</span></span>

### <span data-ttu-id="cda94-122">所有</span><span class="sxs-lookup"><span data-stu-id="cda94-122">None</span></span>

## <span data-ttu-id="cda94-123">輸出</span><span class="sxs-lookup"><span data-stu-id="cda94-123">OUTPUTS</span></span>

### <span data-ttu-id="cda94-124">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="cda94-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="cda94-125">筆記</span><span class="sxs-lookup"><span data-stu-id="cda94-125">NOTES</span></span>

## <span data-ttu-id="cda94-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="cda94-126">RELATED LINKS</span></span>

[<span data-ttu-id="cda94-127">移除-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cda94-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="cda94-128">使用-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cda94-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


