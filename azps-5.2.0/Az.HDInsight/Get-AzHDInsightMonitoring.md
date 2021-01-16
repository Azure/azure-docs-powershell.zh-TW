---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277975"
---
# <span data-ttu-id="95f8b-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="95f8b-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="95f8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="95f8b-103">取得群集上的監視安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="95f8b-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="95f8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="95f8b-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f8b-105">說明</span><span class="sxs-lookup"><span data-stu-id="95f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="95f8b-106">**AzHDInsightMonitoring** Cmdlet 會取得 Azure HDInsight 群集中的監視安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="95f8b-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="95f8b-107">如果啟用監視，也會傳回 log analytics 工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="95f8b-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="95f8b-108">示例</span><span class="sxs-lookup"><span data-stu-id="95f8b-108">EXAMPLES</span></span>

### <span data-ttu-id="95f8b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="95f8b-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="95f8b-110">因為 ClusterMonitoringEnabled 屬性為 true，所以已在群集上啟用監視。</span><span class="sxs-lookup"><span data-stu-id="95f8b-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="95f8b-111">記錄流入位置的監控工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="95f8b-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="95f8b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="95f8b-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="95f8b-113">因為 ClusterMonitoringEnabled 屬性為 true，所以已在群集上啟用監視。</span><span class="sxs-lookup"><span data-stu-id="95f8b-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="95f8b-114">記錄流入位置的監控工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="95f8b-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="95f8b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="95f8b-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="95f8b-116">因為 ClusterMonitoringEnabled 屬性為 false，所以無法在群集上停用監視。</span><span class="sxs-lookup"><span data-stu-id="95f8b-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="95f8b-117">範例4</span><span class="sxs-lookup"><span data-stu-id="95f8b-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="95f8b-118">因為 ClusterMonitoringEnabled 屬性為 false，所以無法在群集上停用監視。</span><span class="sxs-lookup"><span data-stu-id="95f8b-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="95f8b-119">參數</span><span class="sxs-lookup"><span data-stu-id="95f8b-119">PARAMETERS</span></span>

### <span data-ttu-id="95f8b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f8b-120">-DefaultProfile</span></span>
<span data-ttu-id="95f8b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95f8b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95f8b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="95f8b-122">-Name</span></span>
<span data-ttu-id="95f8b-123">要取得監視狀態的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="95f8b-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="95f8b-125">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="95f8b-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f8b-126">CommonParameters</span></span>
<span data-ttu-id="95f8b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95f8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f8b-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95f8b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f8b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="95f8b-129">INPUTS</span></span>

### <span data-ttu-id="95f8b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="95f8b-130">System.String</span></span>

## <span data-ttu-id="95f8b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="95f8b-131">OUTPUTS</span></span>

### <span data-ttu-id="95f8b-132">AzureHDInsightMonitoring 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="95f8b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="95f8b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="95f8b-133">NOTES</span></span>

## <span data-ttu-id="95f8b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="95f8b-134">RELATED LINKS</span></span>
