---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131647"
---
# <span data-ttu-id="0f391-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="0f391-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="0f391-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f391-102">SYNOPSIS</span></span>
<span data-ttu-id="0f391-103">列出 Kusto 資源提供者的合格 Sku。</span><span class="sxs-lookup"><span data-stu-id="0f391-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="0f391-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f391-104">SYNTAX</span></span>

### <span data-ttu-id="0f391-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0f391-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f391-106">List1</span><span class="sxs-lookup"><span data-stu-id="0f391-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0f391-107">說明</span><span class="sxs-lookup"><span data-stu-id="0f391-107">DESCRIPTION</span></span>
<span data-ttu-id="0f391-108">列出 Kusto 資源提供者的合格 Sku。</span><span class="sxs-lookup"><span data-stu-id="0f391-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="0f391-109">示例</span><span class="sxs-lookup"><span data-stu-id="0f391-109">EXAMPLES</span></span>

### <span data-ttu-id="0f391-110">範例1：列出合格的 Sku</span><span class="sxs-lookup"><span data-stu-id="0f391-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="0f391-111">上述命令會列出合格的 Sku。</span><span class="sxs-lookup"><span data-stu-id="0f391-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="0f391-112">範例2：列出特定群集的合格 Sku</span><span class="sxs-lookup"><span data-stu-id="0f391-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="0f391-113">上述命令會列出特定群集的合格 Sku</span><span class="sxs-lookup"><span data-stu-id="0f391-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="0f391-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f391-114">PARAMETERS</span></span>

### <span data-ttu-id="0f391-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0f391-115">-ClusterName</span></span>
<span data-ttu-id="0f391-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f391-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0f391-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f391-117">-DefaultProfile</span></span>
<span data-ttu-id="0f391-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f391-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f391-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f391-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f391-120">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f391-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0f391-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f391-121">-SubscriptionId</span></span>
<span data-ttu-id="0f391-122">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0f391-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f391-123">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0f391-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0f391-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f391-124">CommonParameters</span></span>
<span data-ttu-id="0f391-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f391-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f391-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0f391-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f391-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0f391-127">INPUTS</span></span>

## <span data-ttu-id="0f391-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0f391-128">OUTPUTS</span></span>

### <span data-ttu-id="0f391-129">IAzureResourceSku （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="0f391-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="0f391-130">ISkuDescription （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="0f391-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="0f391-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0f391-131">NOTES</span></span>

<span data-ttu-id="0f391-132">別名</span><span class="sxs-lookup"><span data-stu-id="0f391-132">ALIASES</span></span>

## <span data-ttu-id="0f391-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f391-133">RELATED LINKS</span></span>

