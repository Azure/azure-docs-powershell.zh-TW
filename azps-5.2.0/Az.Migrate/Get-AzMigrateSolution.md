---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284595"
---
# <span data-ttu-id="51e5d-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="51e5d-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="51e5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="51e5d-103">取得 [遷移] 專案中的解決方案。</span><span class="sxs-lookup"><span data-stu-id="51e5d-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="51e5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="51e5d-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="51e5d-105">說明</span><span class="sxs-lookup"><span data-stu-id="51e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="51e5d-106">取得 [遷移] 專案中的解決方案。</span><span class="sxs-lookup"><span data-stu-id="51e5d-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="51e5d-107">示例</span><span class="sxs-lookup"><span data-stu-id="51e5d-107">EXAMPLES</span></span>

### <span data-ttu-id="51e5d-108">範例1：取得</span><span class="sxs-lookup"><span data-stu-id="51e5d-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="51e5d-109">依名稱取得遷移專案方案。</span><span class="sxs-lookup"><span data-stu-id="51e5d-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="51e5d-110">參數</span><span class="sxs-lookup"><span data-stu-id="51e5d-110">PARAMETERS</span></span>

### <span data-ttu-id="51e5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e5d-111">-DefaultProfile</span></span>
<span data-ttu-id="51e5d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51e5d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e5d-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="51e5d-113">-MigrateProjectName</span></span>
<span data-ttu-id="51e5d-114">Azure 遷移專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="51e5d-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="51e5d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="51e5d-115">-Name</span></span>
<span data-ttu-id="51e5d-116">遷移專案中之遷移方案的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="51e5d-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="51e5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="51e5d-118">遷移專案所屬之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="51e5d-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="51e5d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51e5d-119">-SubscriptionId</span></span>
<span data-ttu-id="51e5d-120">在其中建立 [遷移] 專案的 Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="51e5d-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="51e5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e5d-121">CommonParameters</span></span>
<span data-ttu-id="51e5d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51e5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e5d-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="51e5d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e5d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="51e5d-124">INPUTS</span></span>

## <span data-ttu-id="51e5d-125">輸出</span><span class="sxs-lookup"><span data-stu-id="51e5d-125">OUTPUTS</span></span>

### <span data-ttu-id="51e5d-126">ISolution 中的 Api20180901Preview （）。</span><span class="sxs-lookup"><span data-stu-id="51e5d-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="51e5d-127">筆記</span><span class="sxs-lookup"><span data-stu-id="51e5d-127">NOTES</span></span>

<span data-ttu-id="51e5d-128">別名</span><span class="sxs-lookup"><span data-stu-id="51e5d-128">ALIASES</span></span>

## <span data-ttu-id="51e5d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="51e5d-129">RELATED LINKS</span></span>

