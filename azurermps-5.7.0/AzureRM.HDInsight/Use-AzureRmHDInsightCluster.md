---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: c8a58963e66c8260a0001c144230cabf3a80b295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626161"
---
# <span data-ttu-id="359d2-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="359d2-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="359d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="359d2-102">SYNOPSIS</span></span>
<span data-ttu-id="359d2-103">選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。</span><span class="sxs-lookup"><span data-stu-id="359d2-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="359d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="359d2-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="359d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="359d2-105">DESCRIPTION</span></span>
<span data-ttu-id="359d2-106">**AzureRmHDInsightCluster** Cmdlet 會為 Invoke-AzureRmHDInsightHiveJob Cmdlet 選取 Azure HDInsight 群集，以用於提交 Hive 作業。</span><span class="sxs-lookup"><span data-stu-id="359d2-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="359d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="359d2-107">EXAMPLES</span></span>

### <span data-ttu-id="359d2-108">範例1：針對 Hive 查詢提交選取群集</span><span class="sxs-lookup"><span data-stu-id="359d2-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="359d2-109">這個命令會為 Hive 查詢提交選取群集。</span><span class="sxs-lookup"><span data-stu-id="359d2-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="359d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="359d2-110">PARAMETERS</span></span>

### <span data-ttu-id="359d2-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="359d2-111">-ClusterName</span></span>
<span data-ttu-id="359d2-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="359d2-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="359d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359d2-113">-DefaultProfile</span></span>
<span data-ttu-id="359d2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="359d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="359d2-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="359d2-115">-HttpCredential</span></span>
<span data-ttu-id="359d2-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="359d2-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="359d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="359d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="359d2-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="359d2-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="359d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359d2-119">CommonParameters</span></span>
<span data-ttu-id="359d2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="359d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359d2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="359d2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359d2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="359d2-122">INPUTS</span></span>

### <span data-ttu-id="359d2-123">所有</span><span class="sxs-lookup"><span data-stu-id="359d2-123">None</span></span>
<span data-ttu-id="359d2-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="359d2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="359d2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="359d2-125">OUTPUTS</span></span>

### <span data-ttu-id="359d2-126">System.object</span><span class="sxs-lookup"><span data-stu-id="359d2-126">System.String</span></span>

## <span data-ttu-id="359d2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="359d2-127">NOTES</span></span>

## <span data-ttu-id="359d2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="359d2-128">RELATED LINKS</span></span>

[<span data-ttu-id="359d2-129">AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="359d2-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="359d2-130">移除-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="359d2-130">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


