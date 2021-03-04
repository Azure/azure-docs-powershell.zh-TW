---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909618"
---
# <span data-ttu-id="d5d7b-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="d5d7b-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="d5d7b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d5d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d7b-103">初始化要遷移專案的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="d5d7b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d5d7b-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5d7b-105">描述</span><span class="sxs-lookup"><span data-stu-id="d5d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="d5d7b-106">Cmdlet Initialize-AzMigrateReplicationInfrastructure初始化要遷移專案的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="d5d7b-107">例子</span><span class="sxs-lookup"><span data-stu-id="d5d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="d5d7b-108">範例 1：初始化要用於遷移專案的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="d5d7b-109">初始化要遷移專案的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="d5d7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="d5d7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d7b-111">-DefaultProfile</span></span>
<span data-ttu-id="d5d7b-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d7b-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d5d7b-113">-ProjectName</span></span>
<span data-ttu-id="d5d7b-114">指定要用於伺服器移移的 Azure Migration 專案名稱。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="d5d7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5d7b-116">指定目前訂閱中 Azure Migrate Project 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="d5d7b-117">-案例</span><span class="sxs-lookup"><span data-stu-id="d5d7b-117">-Scenario</span></span>
<span data-ttu-id="d5d7b-118">指定需要初始化複製基礎結構的伺服器移移案例。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="d5d7b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5d7b-119">-SubscriptionId</span></span>
<span data-ttu-id="d5d7b-120">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d5d7b-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="d5d7b-121">-TargetRegion</span></span>
<span data-ttu-id="d5d7b-122">指定伺服器移移的目標 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="d5d7b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="d5d7b-123">-Confirm</span></span>
<span data-ttu-id="d5d7b-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d7b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d7b-125">-WhatIf</span></span>
<span data-ttu-id="d5d7b-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5d7b-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d7b-128">CommonParameters</span></span>
<span data-ttu-id="d5d7b-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d5d7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d7b-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5d7b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d7b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d7b-131">INPUTS</span></span>

## <span data-ttu-id="d5d7b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d5d7b-132">OUTPUTS</span></span>

### <span data-ttu-id="d5d7b-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5d7b-133">System.Boolean</span></span>

## <span data-ttu-id="d5d7b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d5d7b-134">NOTES</span></span>

<span data-ttu-id="d5d7b-135">別名</span><span class="sxs-lookup"><span data-stu-id="d5d7b-135">ALIASES</span></span>

## <span data-ttu-id="d5d7b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5d7b-136">RELATED LINKS</span></span>

