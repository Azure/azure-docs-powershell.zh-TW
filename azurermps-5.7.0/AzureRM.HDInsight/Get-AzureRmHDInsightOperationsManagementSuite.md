---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 38c7bfe31faa8b4f167a14ede75f92055919ba55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457172"
---
# <span data-ttu-id="37aa3-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="37aa3-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="37aa3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="37aa3-103">取得群集上 (OMS) 安裝的 Operations Management Suite 狀態。</span><span class="sxs-lookup"><span data-stu-id="37aa3-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37aa3-104">句法</span><span class="sxs-lookup"><span data-stu-id="37aa3-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37aa3-105">說明</span><span class="sxs-lookup"><span data-stu-id="37aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="37aa3-106">**AzureRmHDInsightOperationsManagementSuite** Cmdlet 會取得 Azure HDInsight 群集中的 OMS 安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="37aa3-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="37aa3-107">如果已啟用 OMS，則也會傳回 OMS 工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="37aa3-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="37aa3-108">示例</span><span class="sxs-lookup"><span data-stu-id="37aa3-108">EXAMPLES</span></span>

### <span data-ttu-id="37aa3-109">範例1</span><span class="sxs-lookup"><span data-stu-id="37aa3-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="37aa3-110">ClusterMonitoringEnabled 屬性為 true，因此已在群集上啟用 Operations Management Suite (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="37aa3-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="37aa3-111">記錄流入位置的 OMS 工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="37aa3-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="37aa3-112">範例2</span><span class="sxs-lookup"><span data-stu-id="37aa3-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="37aa3-113">ClusterMonitoringEnabled 屬性為 true，因此已在群集上啟用 Operations Management Suite (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="37aa3-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="37aa3-114">記錄流入位置的 OMS 工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="37aa3-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="37aa3-115">範例3</span><span class="sxs-lookup"><span data-stu-id="37aa3-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="37aa3-116">因為 ClusterMonitoringEnabled 屬性為 false，所以在群集上停用運營管理套件 (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="37aa3-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="37aa3-117">範例4</span><span class="sxs-lookup"><span data-stu-id="37aa3-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="37aa3-118">因為 ClusterMonitoringEnabled 屬性為 false，所以在群集上停用運營管理套件 (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="37aa3-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="37aa3-119">參數</span><span class="sxs-lookup"><span data-stu-id="37aa3-119">PARAMETERS</span></span>

### <span data-ttu-id="37aa3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37aa3-120">-DefaultProfile</span></span>
<span data-ttu-id="37aa3-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="37aa3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37aa3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="37aa3-122">-Name</span></span>
<span data-ttu-id="37aa3-123">要取得作業管理套件狀態的群集名稱 (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="37aa3-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37aa3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37aa3-124">-ResourceGroupName</span></span>
<span data-ttu-id="37aa3-125">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="37aa3-125">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37aa3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37aa3-126">CommonParameters</span></span>
<span data-ttu-id="37aa3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37aa3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37aa3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37aa3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37aa3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="37aa3-129">INPUTS</span></span>

### <span data-ttu-id="37aa3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="37aa3-130">System.String</span></span>

## <span data-ttu-id="37aa3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="37aa3-131">OUTPUTS</span></span>

### <span data-ttu-id="37aa3-132">AzureHDInsightOMS 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="37aa3-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="37aa3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="37aa3-133">NOTES</span></span>

## <span data-ttu-id="37aa3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="37aa3-134">RELATED LINKS</span></span>

