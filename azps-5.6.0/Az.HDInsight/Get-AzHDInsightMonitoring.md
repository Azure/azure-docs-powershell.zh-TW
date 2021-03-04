---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916567"
---
# <span data-ttu-id="02936-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="02936-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="02936-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02936-102">SYNOPSIS</span></span>
<span data-ttu-id="02936-103">在組集中獲得監控安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="02936-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="02936-104">語法</span><span class="sxs-lookup"><span data-stu-id="02936-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02936-105">描述</span><span class="sxs-lookup"><span data-stu-id="02936-105">DESCRIPTION</span></span>
<span data-ttu-id="02936-106">**Get-AzHDInsightMonitoring** Cmdlet 會取得 Azure HDInsight 組集中的監控安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="02936-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="02936-107">如果已啟用監控，它也將會返回記錄分析工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="02936-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="02936-108">例子</span><span class="sxs-lookup"><span data-stu-id="02936-108">EXAMPLES</span></span>

### <span data-ttu-id="02936-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="02936-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="02936-110">由於 ClusterMonitoringEnabled 屬性為 True，因此會啟用在組集中監控。</span><span class="sxs-lookup"><span data-stu-id="02936-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="02936-111">記錄正在移動的監控工作區識別碼為 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="02936-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="02936-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="02936-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="02936-113">由於 ClusterMonitoringEnabled 屬性為 True，因此會啟用在組集中監控。</span><span class="sxs-lookup"><span data-stu-id="02936-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="02936-114">記錄正在移動的監控工作區識別碼為 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="02936-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="02936-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="02936-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="02936-116">由於 ClusterMonitoringEnabled 屬性為 False，因此會停用該組集中的監控功能。</span><span class="sxs-lookup"><span data-stu-id="02936-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="02936-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="02936-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="02936-118">由於 ClusterMonitoringEnabled 屬性為 False，因此會停用該組集中的監控功能。</span><span class="sxs-lookup"><span data-stu-id="02936-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="02936-119">參數</span><span class="sxs-lookup"><span data-stu-id="02936-119">PARAMETERS</span></span>

### <span data-ttu-id="02936-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02936-120">-DefaultProfile</span></span>
<span data-ttu-id="02936-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="02936-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02936-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="02936-122">-Name</span></span>
<span data-ttu-id="02936-123">取得監控狀態的組名。</span><span class="sxs-lookup"><span data-stu-id="02936-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="02936-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02936-124">-ResourceGroupName</span></span>
<span data-ttu-id="02936-125">群組的資源群組。</span><span class="sxs-lookup"><span data-stu-id="02936-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="02936-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02936-126">CommonParameters</span></span>
<span data-ttu-id="02936-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02936-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02936-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02936-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02936-129">輸入</span><span class="sxs-lookup"><span data-stu-id="02936-129">INPUTS</span></span>

### <span data-ttu-id="02936-130">System.String</span><span class="sxs-lookup"><span data-stu-id="02936-130">System.String</span></span>

## <span data-ttu-id="02936-131">輸出</span><span class="sxs-lookup"><span data-stu-id="02936-131">OUTPUTS</span></span>

### <span data-ttu-id="02936-132">Microsoft.Azure.Commands.HDInsight.Models.management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="02936-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="02936-133">筆記</span><span class="sxs-lookup"><span data-stu-id="02936-133">NOTES</span></span>

## <span data-ttu-id="02936-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="02936-134">RELATED LINKS</span></span>
