---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: bc78b7d791d0988ee692c12537aed3207066ba26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913774"
---
# <span data-ttu-id="abb72-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="abb72-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="abb72-102">簡介</span><span class="sxs-lookup"><span data-stu-id="abb72-102">SYNOPSIS</span></span>
<span data-ttu-id="abb72-103">取得或列出組群</span><span class="sxs-lookup"><span data-stu-id="abb72-103">Get or list clusters</span></span>

## <span data-ttu-id="abb72-104">語法</span><span class="sxs-lookup"><span data-stu-id="abb72-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb72-105">描述</span><span class="sxs-lookup"><span data-stu-id="abb72-105">DESCRIPTION</span></span>
<span data-ttu-id="abb72-106">取得或列出群組、未提供 「-ClusterName」時，在資源群組下的清單群組、未提供 「-ClusterName」和「ResourceGroupName」時訂閱下的清單群組。</span><span class="sxs-lookup"><span data-stu-id="abb72-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="abb72-107">例子</span><span class="sxs-lookup"><span data-stu-id="abb72-107">EXAMPLES</span></span>

### <span data-ttu-id="abb72-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="abb72-108">Example 1</span></span>
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

<span data-ttu-id="abb72-109">取得集區</span><span class="sxs-lookup"><span data-stu-id="abb72-109">Get cluster</span></span>

## <span data-ttu-id="abb72-110">參數</span><span class="sxs-lookup"><span data-stu-id="abb72-110">PARAMETERS</span></span>

### <span data-ttu-id="abb72-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="abb72-111">-ClusterName</span></span>
<span data-ttu-id="abb72-112">組名。</span><span class="sxs-lookup"><span data-stu-id="abb72-112">The cluster name.</span></span>

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

### <span data-ttu-id="abb72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb72-113">-DefaultProfile</span></span>
<span data-ttu-id="abb72-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="abb72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abb72-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb72-115">-ResourceGroupName</span></span>
<span data-ttu-id="abb72-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="abb72-116">The resource group name.</span></span>

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

### <span data-ttu-id="abb72-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb72-117">CommonParameters</span></span>
<span data-ttu-id="abb72-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="abb72-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb72-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abb72-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb72-120">輸入</span><span class="sxs-lookup"><span data-stu-id="abb72-120">INPUTS</span></span>

### <span data-ttu-id="abb72-121">System.String</span><span class="sxs-lookup"><span data-stu-id="abb72-121">System.String</span></span>

## <span data-ttu-id="abb72-122">輸出</span><span class="sxs-lookup"><span data-stu-id="abb72-122">OUTPUTS</span></span>

### <span data-ttu-id="abb72-123">Microsoft.Azure.Commands.OperationalInsights.models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="abb72-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="abb72-124">筆記</span><span class="sxs-lookup"><span data-stu-id="abb72-124">NOTES</span></span>

## <span data-ttu-id="abb72-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="abb72-125">RELATED LINKS</span></span>
