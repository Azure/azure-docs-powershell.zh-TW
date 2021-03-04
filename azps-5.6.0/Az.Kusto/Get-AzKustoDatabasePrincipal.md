---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 3380835b4ca8e51c8ba0952ef3ef4bd973fadea3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902038"
---
# <span data-ttu-id="462ca-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="462ca-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="462ca-102">簡介</span><span class="sxs-lookup"><span data-stu-id="462ca-102">SYNOPSIS</span></span>
<span data-ttu-id="462ca-103">會返回給定 Kusto 集和資料庫的資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="462ca-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="462ca-104">語法</span><span class="sxs-lookup"><span data-stu-id="462ca-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="462ca-105">描述</span><span class="sxs-lookup"><span data-stu-id="462ca-105">DESCRIPTION</span></span>
<span data-ttu-id="462ca-106">會返回給定 Kusto 集和資料庫的資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="462ca-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="462ca-107">例子</span><span class="sxs-lookup"><span data-stu-id="462ca-107">EXAMPLES</span></span>

### <span data-ttu-id="462ca-108">範例 1：給定 Kusto 組和資料庫的資料庫主體清單</span><span class="sxs-lookup"><span data-stu-id="462ca-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="462ca-109">上述命令會返回給定 Kusto 集區與資料庫的資料庫主體清單</span><span class="sxs-lookup"><span data-stu-id="462ca-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="462ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="462ca-110">PARAMETERS</span></span>

### <span data-ttu-id="462ca-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="462ca-111">-ClusterName</span></span>
<span data-ttu-id="462ca-112">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="462ca-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="462ca-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="462ca-113">-DatabaseName</span></span>
<span data-ttu-id="462ca-114">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="462ca-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="462ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462ca-115">-DefaultProfile</span></span>
<span data-ttu-id="462ca-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="462ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="462ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="462ca-118">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="462ca-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="462ca-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="462ca-119">-SubscriptionId</span></span>
<span data-ttu-id="462ca-120">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="462ca-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="462ca-121">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="462ca-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="462ca-122">-確認</span><span class="sxs-lookup"><span data-stu-id="462ca-122">-Confirm</span></span>
<span data-ttu-id="462ca-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="462ca-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462ca-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462ca-124">-WhatIf</span></span>
<span data-ttu-id="462ca-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="462ca-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462ca-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="462ca-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462ca-127">CommonParameters</span></span>
<span data-ttu-id="462ca-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="462ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462ca-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="462ca-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462ca-130">輸入</span><span class="sxs-lookup"><span data-stu-id="462ca-130">INPUTS</span></span>

## <span data-ttu-id="462ca-131">輸出</span><span class="sxs-lookup"><span data-stu-id="462ca-131">OUTPUTS</span></span>

### <span data-ttu-id="462ca-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="462ca-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="462ca-133">筆記</span><span class="sxs-lookup"><span data-stu-id="462ca-133">NOTES</span></span>

<span data-ttu-id="462ca-134">別名</span><span class="sxs-lookup"><span data-stu-id="462ca-134">ALIASES</span></span>

## <span data-ttu-id="462ca-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="462ca-135">RELATED LINKS</span></span>

