---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971412"
---
# <span data-ttu-id="d9141-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="d9141-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="d9141-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9141-102">SYNOPSIS</span></span>
<span data-ttu-id="d9141-103">列出 Kusto 資源提供者的合格 Sku。</span><span class="sxs-lookup"><span data-stu-id="d9141-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d9141-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9141-104">SYNTAX</span></span>

### <span data-ttu-id="d9141-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="d9141-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9141-106">List1</span><span class="sxs-lookup"><span data-stu-id="d9141-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9141-107">說明</span><span class="sxs-lookup"><span data-stu-id="d9141-107">DESCRIPTION</span></span>
<span data-ttu-id="d9141-108">列出 Kusto 資源提供者的合格 Sku。</span><span class="sxs-lookup"><span data-stu-id="d9141-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d9141-109">示例</span><span class="sxs-lookup"><span data-stu-id="d9141-109">EXAMPLES</span></span>

### <span data-ttu-id="d9141-110">範例1：列出合格的 Sku</span><span class="sxs-lookup"><span data-stu-id="d9141-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="d9141-111">上述命令會列出合格的 Sku。</span><span class="sxs-lookup"><span data-stu-id="d9141-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="d9141-112">範例2：列出特定群集的合格 Sku</span><span class="sxs-lookup"><span data-stu-id="d9141-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="d9141-113">上述命令會列出特定群集的合格 Sku</span><span class="sxs-lookup"><span data-stu-id="d9141-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="d9141-114">參數</span><span class="sxs-lookup"><span data-stu-id="d9141-114">PARAMETERS</span></span>

### <span data-ttu-id="d9141-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d9141-115">-ClusterName</span></span>
<span data-ttu-id="d9141-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9141-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9141-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9141-117">-DefaultProfile</span></span>
<span data-ttu-id="d9141-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9141-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9141-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9141-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9141-120">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9141-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9141-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9141-121">-SubscriptionId</span></span>
<span data-ttu-id="d9141-122">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d9141-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9141-123">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d9141-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9141-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9141-124">CommonParameters</span></span>
<span data-ttu-id="d9141-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9141-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9141-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9141-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9141-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d9141-127">INPUTS</span></span>

## <span data-ttu-id="d9141-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d9141-128">OUTPUTS</span></span>

### <span data-ttu-id="d9141-129">IAzureResourceSku （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="d9141-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="d9141-130">ISkuDescription （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="d9141-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="d9141-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d9141-131">NOTES</span></span>

<span data-ttu-id="d9141-132">別名</span><span class="sxs-lookup"><span data-stu-id="d9141-132">ALIASES</span></span>

## <span data-ttu-id="d9141-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9141-133">RELATED LINKS</span></span>

