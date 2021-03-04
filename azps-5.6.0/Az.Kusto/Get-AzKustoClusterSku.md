---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 4b72dde837122329a4761fc0c2c1a0120914e60f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905038"
---
# <span data-ttu-id="91abd-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="91abd-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="91abd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91abd-102">SYNOPSIS</span></span>
<span data-ttu-id="91abd-103">列出適用于 Kusto 資源提供者的合格 SKU。</span><span class="sxs-lookup"><span data-stu-id="91abd-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="91abd-104">語法</span><span class="sxs-lookup"><span data-stu-id="91abd-104">SYNTAX</span></span>

### <span data-ttu-id="91abd-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="91abd-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91abd-106">清單1</span><span class="sxs-lookup"><span data-stu-id="91abd-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91abd-107">描述</span><span class="sxs-lookup"><span data-stu-id="91abd-107">DESCRIPTION</span></span>
<span data-ttu-id="91abd-108">列出適用于 Kusto 資源提供者的合格 SKU。</span><span class="sxs-lookup"><span data-stu-id="91abd-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="91abd-109">例子</span><span class="sxs-lookup"><span data-stu-id="91abd-109">EXAMPLES</span></span>

### <span data-ttu-id="91abd-110">範例 1：列出符合資格的 SKUS</span><span class="sxs-lookup"><span data-stu-id="91abd-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="91abd-111">上述命令會列出符合資格的 SKUS。</span><span class="sxs-lookup"><span data-stu-id="91abd-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="91abd-112">範例 2：列出特定組群的合格 SKUS</span><span class="sxs-lookup"><span data-stu-id="91abd-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="91abd-113">上述命令列出適用于特定組群的合格 SKUS</span><span class="sxs-lookup"><span data-stu-id="91abd-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="91abd-114">參數</span><span class="sxs-lookup"><span data-stu-id="91abd-114">PARAMETERS</span></span>

### <span data-ttu-id="91abd-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="91abd-115">-ClusterName</span></span>
<span data-ttu-id="91abd-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="91abd-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91abd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91abd-117">-DefaultProfile</span></span>
<span data-ttu-id="91abd-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="91abd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91abd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91abd-119">-ResourceGroupName</span></span>
<span data-ttu-id="91abd-120">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="91abd-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91abd-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91abd-121">-SubscriptionId</span></span>
<span data-ttu-id="91abd-122">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="91abd-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="91abd-123">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="91abd-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91abd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91abd-124">CommonParameters</span></span>
<span data-ttu-id="91abd-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91abd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91abd-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91abd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91abd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="91abd-127">INPUTS</span></span>

## <span data-ttu-id="91abd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="91abd-128">OUTPUTS</span></span>

### <span data-ttu-id="91abd-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="91abd-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="91abd-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="91abd-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="91abd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="91abd-131">NOTES</span></span>

<span data-ttu-id="91abd-132">別名</span><span class="sxs-lookup"><span data-stu-id="91abd-132">ALIASES</span></span>

## <span data-ttu-id="91abd-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="91abd-133">RELATED LINKS</span></span>

