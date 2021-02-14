---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 09284a91c5ea2f7561a867250a92c4cd0d96e8e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142994"
---
# <span data-ttu-id="41870-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="41870-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="41870-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41870-102">SYNOPSIS</span></span>
<span data-ttu-id="41870-103">建立或更新已附加的資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="41870-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="41870-104">句法</span><span class="sxs-lookup"><span data-stu-id="41870-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41870-105">說明</span><span class="sxs-lookup"><span data-stu-id="41870-105">DESCRIPTION</span></span>
<span data-ttu-id="41870-106">建立或更新已附加的資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="41870-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="41870-107">示例</span><span class="sxs-lookup"><span data-stu-id="41870-107">EXAMPLES</span></span>

### <span data-ttu-id="41870-108">範例1：建立新的 AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="41870-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="41870-109">上述命令會在群集 "testnewkustoclusterf" 中建立 ReadOnly 資料庫 "mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="41870-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="41870-110">它跟來自群集 "testnewkustocluster" 的資料庫 "mykustodatabase"</span><span class="sxs-lookup"><span data-stu-id="41870-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="41870-111">參數</span><span class="sxs-lookup"><span data-stu-id="41870-111">PARAMETERS</span></span>

### <span data-ttu-id="41870-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41870-112">-AsJob</span></span>
<span data-ttu-id="41870-113">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="41870-113">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41870-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="41870-114">-ClusterName</span></span>
<span data-ttu-id="41870-115">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="41870-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="41870-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="41870-116">-ClusterResourceId</span></span>
<span data-ttu-id="41870-117">您想要附加的資料庫所在之群集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="41870-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="41870-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41870-118">-DatabaseName</span></span>
<span data-ttu-id="41870-119">您想要附加的資料庫名稱，請使用 \* （如果您想要追蹤所有目前及未來的資料庫）。</span><span class="sxs-lookup"><span data-stu-id="41870-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="41870-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="41870-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="41870-121">預設主體修改類型</span><span class="sxs-lookup"><span data-stu-id="41870-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41870-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41870-122">-DefaultProfile</span></span>
<span data-ttu-id="41870-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41870-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41870-124">-位置</span><span class="sxs-lookup"><span data-stu-id="41870-124">-Location</span></span>
<span data-ttu-id="41870-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="41870-125">Resource location.</span></span>

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

### <span data-ttu-id="41870-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="41870-126">-Name</span></span>
<span data-ttu-id="41870-127">已附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="41870-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41870-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="41870-128">-NoWait</span></span>
<span data-ttu-id="41870-129">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="41870-129">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41870-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41870-130">-ResourceGroupName</span></span>
<span data-ttu-id="41870-131">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41870-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="41870-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41870-132">-SubscriptionId</span></span>
<span data-ttu-id="41870-133">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="41870-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41870-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="41870-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41870-135">-確認</span><span class="sxs-lookup"><span data-stu-id="41870-135">-Confirm</span></span>
<span data-ttu-id="41870-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41870-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41870-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41870-137">-WhatIf</span></span>
<span data-ttu-id="41870-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41870-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41870-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41870-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41870-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41870-140">CommonParameters</span></span>
<span data-ttu-id="41870-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41870-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41870-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41870-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41870-143">輸入</span><span class="sxs-lookup"><span data-stu-id="41870-143">INPUTS</span></span>

## <span data-ttu-id="41870-144">輸出</span><span class="sxs-lookup"><span data-stu-id="41870-144">OUTPUTS</span></span>

### <span data-ttu-id="41870-145">IAttachedDatabaseConfiguration （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="41870-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="41870-146">筆記</span><span class="sxs-lookup"><span data-stu-id="41870-146">NOTES</span></span>

<span data-ttu-id="41870-147">別名</span><span class="sxs-lookup"><span data-stu-id="41870-147">ALIASES</span></span>

## <span data-ttu-id="41870-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="41870-148">RELATED LINKS</span></span>

