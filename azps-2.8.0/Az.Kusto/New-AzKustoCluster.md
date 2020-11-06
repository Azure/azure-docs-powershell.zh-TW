---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9157c5dfff46893cfee88d02d8f1564801f889fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612053"
---
# <span data-ttu-id="f52e7-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="f52e7-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="f52e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f52e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f52e7-103">建立新的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="f52e7-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="f52e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="f52e7-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f52e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="f52e7-105">DESCRIPTION</span></span>
<span data-ttu-id="f52e7-106">建立新的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="f52e7-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="f52e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="f52e7-107">EXAMPLES</span></span>

### <span data-ttu-id="f52e7-108">範例 1-建立新的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="f52e7-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="f52e7-109">上述命令會在資源群組 "testrg" 中建立名為 "mykustocluster" 的新 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="f52e7-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="f52e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="f52e7-110">PARAMETERS</span></span>

### <span data-ttu-id="f52e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52e7-111">-DefaultProfile</span></span>
<span data-ttu-id="f52e7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f52e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52e7-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f52e7-113">-Location</span></span>
<span data-ttu-id="f52e7-114">應建立群集的 Azure 地區。</span><span class="sxs-lookup"><span data-stu-id="f52e7-114">Azure region where the cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f52e7-115">-Name</span></span>
<span data-ttu-id="f52e7-116">要建立之群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f52e7-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="f52e7-118">您要在其中建立群集的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f52e7-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="f52e7-119">-Sku</span></span>
<span data-ttu-id="f52e7-120">用來建立群集的 Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="f52e7-120">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="f52e7-121">-Tag</span></span>
<span data-ttu-id="f52e7-122">與此群集相關聯之標記的字串字典</span><span class="sxs-lookup"><span data-stu-id="f52e7-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-123">層級</span><span class="sxs-lookup"><span data-stu-id="f52e7-123">-Tier</span></span>
<span data-ttu-id="f52e7-124">建立群集所用的層級名稱</span><span class="sxs-lookup"><span data-stu-id="f52e7-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f52e7-125">-Confirm</span></span>
<span data-ttu-id="f52e7-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f52e7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52e7-127">-WhatIf</span></span>
<span data-ttu-id="f52e7-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f52e7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f52e7-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f52e7-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52e7-130">CommonParameters</span></span>
<span data-ttu-id="f52e7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f52e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52e7-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f52e7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52e7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f52e7-133">INPUTS</span></span>

### <span data-ttu-id="f52e7-134">所有</span><span class="sxs-lookup"><span data-stu-id="f52e7-134">None</span></span>

## <span data-ttu-id="f52e7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f52e7-135">OUTPUTS</span></span>

### <span data-ttu-id="f52e7-136">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="f52e7-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="f52e7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f52e7-137">NOTES</span></span>

## <span data-ttu-id="f52e7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f52e7-138">RELATED LINKS</span></span>
