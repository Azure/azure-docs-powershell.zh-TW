---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971416"
---
# <span data-ttu-id="4768f-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="4768f-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="4768f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4768f-102">SYNOPSIS</span></span>
<span data-ttu-id="4768f-103">傳回這個群集擁有的資料庫清單，後面接著另一個群集。</span><span class="sxs-lookup"><span data-stu-id="4768f-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="4768f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4768f-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4768f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4768f-105">DESCRIPTION</span></span>
<span data-ttu-id="4768f-106">傳回這個群集擁有的資料庫清單，後面接著另一個群集。</span><span class="sxs-lookup"><span data-stu-id="4768f-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="4768f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4768f-107">EXAMPLES</span></span>

### <span data-ttu-id="4768f-108">範例1：列出所有追蹤的資料庫</span><span class="sxs-lookup"><span data-stu-id="4768f-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="4768f-109">上述命令會列出此群集擁有的所有資料庫，且後面接著另一個群集。</span><span class="sxs-lookup"><span data-stu-id="4768f-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="4768f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4768f-110">PARAMETERS</span></span>

### <span data-ttu-id="4768f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4768f-111">-ClusterName</span></span>
<span data-ttu-id="4768f-112">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4768f-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4768f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4768f-113">-DefaultProfile</span></span>
<span data-ttu-id="4768f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4768f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4768f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4768f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4768f-116">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4768f-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4768f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4768f-117">-SubscriptionId</span></span>
<span data-ttu-id="4768f-118">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4768f-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4768f-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4768f-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4768f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="4768f-120">-Confirm</span></span>
<span data-ttu-id="4768f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4768f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4768f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4768f-122">-WhatIf</span></span>
<span data-ttu-id="4768f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4768f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4768f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4768f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4768f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4768f-125">CommonParameters</span></span>
<span data-ttu-id="4768f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4768f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4768f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4768f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4768f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4768f-128">INPUTS</span></span>

## <span data-ttu-id="4768f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4768f-129">OUTPUTS</span></span>

### <span data-ttu-id="4768f-130">IFollowerDatabaseDefinition （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="4768f-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="4768f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4768f-131">NOTES</span></span>

<span data-ttu-id="4768f-132">別名</span><span class="sxs-lookup"><span data-stu-id="4768f-132">ALIASES</span></span>

## <span data-ttu-id="4768f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4768f-133">RELATED LINKS</span></span>
