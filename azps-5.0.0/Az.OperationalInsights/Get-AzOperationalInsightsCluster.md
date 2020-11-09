---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288132"
---
# <span data-ttu-id="ac9bd-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="ac9bd-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="ac9bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9bd-103">取得或列出群集</span><span class="sxs-lookup"><span data-stu-id="ac9bd-103">Get or list clusters</span></span>

## <span data-ttu-id="ac9bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac9bd-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac9bd-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9bd-106">[取得或列出群集]、[資源群組] 下的 [清單群集] 如果未提供 "-ClusterName"，則在未提供 "-ClusterName" 和 "ResourceGroupName" 時，列出 [訂閱] 下的 [群集]。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="ac9bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac9bd-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9bd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ac9bd-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="ac9bd-109">取得群集</span><span class="sxs-lookup"><span data-stu-id="ac9bd-109">Get cluster</span></span>

## <span data-ttu-id="ac9bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac9bd-110">PARAMETERS</span></span>

### <span data-ttu-id="ac9bd-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ac9bd-111">-ClusterName</span></span>
<span data-ttu-id="ac9bd-112">[群集名稱]。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9bd-113">-DefaultProfile</span></span>
<span data-ttu-id="ac9bd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9bd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9bd-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac9bd-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9bd-117">CommonParameters</span></span>
<span data-ttu-id="ac9bd-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9bd-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9bd-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ac9bd-120">INPUTS</span></span>

### <span data-ttu-id="ac9bd-121">System.object</span><span class="sxs-lookup"><span data-stu-id="ac9bd-121">System.String</span></span>

## <span data-ttu-id="ac9bd-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ac9bd-122">OUTPUTS</span></span>

### <span data-ttu-id="ac9bd-123">PSCluster 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="ac9bd-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="ac9bd-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ac9bd-124">NOTES</span></span>

## <span data-ttu-id="ac9bd-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac9bd-125">RELATED LINKS</span></span>
