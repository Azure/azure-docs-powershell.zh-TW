---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612308"
---
# <span data-ttu-id="acc3b-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="acc3b-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="acc3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="acc3b-103">取得群集上 (OMS) 安裝的 Operations Management Suite 狀態。</span><span class="sxs-lookup"><span data-stu-id="acc3b-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="acc3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="acc3b-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="acc3b-105">DESCRIPTION</span></span>
<span data-ttu-id="acc3b-106">**AzHDInsightOperationsManagementSuite** Cmdlet 會取得 Azure HDInsight 群集中的 OMS 安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="acc3b-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="acc3b-107">如果已啟用 OMS，則也會傳回 OMS 工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="acc3b-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="acc3b-108">示例</span><span class="sxs-lookup"><span data-stu-id="acc3b-108">EXAMPLES</span></span>

### <span data-ttu-id="acc3b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="acc3b-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="acc3b-110">ClusterMonitoringEnabled 屬性為 true，因此已在群集上啟用 Operations Management Suite (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="acc3b-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="acc3b-111">記錄流入位置的 OMS 工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="acc3b-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="acc3b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="acc3b-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="acc3b-113">ClusterMonitoringEnabled 屬性為 true，因此已在群集上啟用 Operations Management Suite (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="acc3b-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="acc3b-114">記錄流入位置的 OMS 工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="acc3b-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="acc3b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="acc3b-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="acc3b-116">因為 ClusterMonitoringEnabled 屬性為 false，所以在群集上停用運營管理套件 (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="acc3b-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="acc3b-117">範例4</span><span class="sxs-lookup"><span data-stu-id="acc3b-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="acc3b-118">因為 ClusterMonitoringEnabled 屬性為 false，所以在群集上停用運營管理套件 (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="acc3b-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="acc3b-119">參數</span><span class="sxs-lookup"><span data-stu-id="acc3b-119">PARAMETERS</span></span>

### <span data-ttu-id="acc3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc3b-120">-DefaultProfile</span></span>
<span data-ttu-id="acc3b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="acc3b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acc3b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="acc3b-122">-Name</span></span>
<span data-ttu-id="acc3b-123">要取得作業管理套件狀態的群集名稱 (OMS) 。</span><span class="sxs-lookup"><span data-stu-id="acc3b-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acc3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="acc3b-125">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="acc3b-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="acc3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc3b-126">CommonParameters</span></span>
<span data-ttu-id="acc3b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acc3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc3b-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acc3b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc3b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="acc3b-129">INPUTS</span></span>

### <span data-ttu-id="acc3b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="acc3b-130">System.String</span></span>

## <span data-ttu-id="acc3b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="acc3b-131">OUTPUTS</span></span>

### <span data-ttu-id="acc3b-132">AzureHDInsightOMS 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="acc3b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="acc3b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="acc3b-133">NOTES</span></span>

## <span data-ttu-id="acc3b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="acc3b-134">RELATED LINKS</span></span>
