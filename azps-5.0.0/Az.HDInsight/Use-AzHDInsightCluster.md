---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139274"
---
# <span data-ttu-id="b456f-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b456f-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="b456f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b456f-102">SYNOPSIS</span></span>
<span data-ttu-id="b456f-103">選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。</span><span class="sxs-lookup"><span data-stu-id="b456f-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="b456f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b456f-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b456f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b456f-105">DESCRIPTION</span></span>
<span data-ttu-id="b456f-106">**AzHDInsightCluster** Cmdlet 會為 Invoke-AzHDInsightHiveJob Cmdlet 選取 Azure HDInsight 群集，以用於提交 Hive 作業。</span><span class="sxs-lookup"><span data-stu-id="b456f-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="b456f-107">示例</span><span class="sxs-lookup"><span data-stu-id="b456f-107">EXAMPLES</span></span>

### <span data-ttu-id="b456f-108">範例1：針對 Hive 查詢提交選取群集</span><span class="sxs-lookup"><span data-stu-id="b456f-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b456f-109">這個命令會為 Hive 查詢提交選取群集。</span><span class="sxs-lookup"><span data-stu-id="b456f-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="b456f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b456f-110">PARAMETERS</span></span>

### <span data-ttu-id="b456f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b456f-111">-ClusterName</span></span>
<span data-ttu-id="b456f-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b456f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b456f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b456f-113">-DefaultProfile</span></span>
<span data-ttu-id="b456f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b456f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b456f-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b456f-115">-HttpCredential</span></span>
<span data-ttu-id="b456f-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="b456f-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b456f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b456f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b456f-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b456f-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b456f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b456f-119">CommonParameters</span></span>
<span data-ttu-id="b456f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b456f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b456f-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b456f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b456f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b456f-122">INPUTS</span></span>

### <span data-ttu-id="b456f-123">所有</span><span class="sxs-lookup"><span data-stu-id="b456f-123">None</span></span>

## <span data-ttu-id="b456f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b456f-124">OUTPUTS</span></span>

### <span data-ttu-id="b456f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="b456f-125">System.String</span></span>

## <span data-ttu-id="b456f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b456f-126">NOTES</span></span>

## <span data-ttu-id="b456f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b456f-127">RELATED LINKS</span></span>

[<span data-ttu-id="b456f-128">AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b456f-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="b456f-129">移除-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b456f-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

