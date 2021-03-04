---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: c3829997703feb0ca3098dfd7bc314b71d5b5d5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909621"
---
# <span data-ttu-id="d7288-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="d7288-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="d7288-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7288-102">SYNOPSIS</span></span>
<span data-ttu-id="d7288-103">在遷移專案中獲得解決方案。</span><span class="sxs-lookup"><span data-stu-id="d7288-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="d7288-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7288-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d7288-105">描述</span><span class="sxs-lookup"><span data-stu-id="d7288-105">DESCRIPTION</span></span>
<span data-ttu-id="d7288-106">在遷移專案中獲得解決方案。</span><span class="sxs-lookup"><span data-stu-id="d7288-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="d7288-107">例子</span><span class="sxs-lookup"><span data-stu-id="d7288-107">EXAMPLES</span></span>

### <span data-ttu-id="d7288-108">範例 1：取得</span><span class="sxs-lookup"><span data-stu-id="d7288-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="d7288-109">取得按名稱進行專案遷移的解決方案。</span><span class="sxs-lookup"><span data-stu-id="d7288-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="d7288-110">參數</span><span class="sxs-lookup"><span data-stu-id="d7288-110">PARAMETERS</span></span>

### <span data-ttu-id="d7288-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7288-111">-DefaultProfile</span></span>
<span data-ttu-id="d7288-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7288-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7288-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="d7288-113">-MigrateProjectName</span></span>
<span data-ttu-id="d7288-114">Azure Migrate 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7288-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="d7288-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7288-115">-Name</span></span>
<span data-ttu-id="d7288-116">移移專案中移移解決方案的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d7288-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7288-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7288-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7288-118">其中一部分是要遷移專案的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="d7288-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="d7288-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7288-119">-SubscriptionId</span></span>
<span data-ttu-id="d7288-120">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7288-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d7288-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7288-121">CommonParameters</span></span>
<span data-ttu-id="d7288-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7288-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7288-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7288-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7288-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d7288-124">INPUTS</span></span>

## <span data-ttu-id="d7288-125">輸出</span><span class="sxs-lookup"><span data-stu-id="d7288-125">OUTPUTS</span></span>

### <span data-ttu-id="d7288-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="d7288-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="d7288-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d7288-127">NOTES</span></span>

<span data-ttu-id="d7288-128">別名</span><span class="sxs-lookup"><span data-stu-id="d7288-128">ALIASES</span></span>

## <span data-ttu-id="d7288-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7288-129">RELATED LINKS</span></span>

