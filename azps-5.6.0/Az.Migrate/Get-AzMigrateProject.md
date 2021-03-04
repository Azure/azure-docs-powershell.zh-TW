---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 4176b07f8a19538a05899b526d21f21cfcc20c9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909658"
---
# <span data-ttu-id="9343c-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="9343c-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="9343c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9343c-102">SYNOPSIS</span></span>
<span data-ttu-id="9343c-103">取得專案遷移的方法。</span><span class="sxs-lookup"><span data-stu-id="9343c-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="9343c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9343c-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9343c-105">描述</span><span class="sxs-lookup"><span data-stu-id="9343c-105">DESCRIPTION</span></span>
<span data-ttu-id="9343c-106">取得專案遷移的方法。</span><span class="sxs-lookup"><span data-stu-id="9343c-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="9343c-107">例子</span><span class="sxs-lookup"><span data-stu-id="9343c-107">EXAMPLES</span></span>

### <span data-ttu-id="9343c-108">範例 1：取得</span><span class="sxs-lookup"><span data-stu-id="9343c-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="9343c-109">取得專案遷移的方法。</span><span class="sxs-lookup"><span data-stu-id="9343c-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="9343c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9343c-110">PARAMETERS</span></span>

### <span data-ttu-id="9343c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9343c-111">-DefaultProfile</span></span>
<span data-ttu-id="9343c-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9343c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9343c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9343c-113">-Name</span></span>
<span data-ttu-id="9343c-114">Azure Migrate 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="9343c-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9343c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9343c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9343c-116">其中一部分是要遷移專案的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="9343c-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="9343c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9343c-117">-SubscriptionId</span></span>
<span data-ttu-id="9343c-118">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9343c-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="9343c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9343c-119">CommonParameters</span></span>
<span data-ttu-id="9343c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9343c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9343c-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9343c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9343c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9343c-122">INPUTS</span></span>

## <span data-ttu-id="9343c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9343c-123">OUTPUTS</span></span>

### <span data-ttu-id="9343c-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="9343c-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="9343c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9343c-125">NOTES</span></span>

<span data-ttu-id="9343c-126">別名</span><span class="sxs-lookup"><span data-stu-id="9343c-126">ALIASES</span></span>

## <span data-ttu-id="9343c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9343c-127">RELATED LINKS</span></span>

