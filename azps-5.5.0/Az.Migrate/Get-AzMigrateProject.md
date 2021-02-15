---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142270"
---
# <span data-ttu-id="1ec8d-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="1ec8d-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="1ec8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ec8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec8d-103">取得遷移專案的方法。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="1ec8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ec8d-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1ec8d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ec8d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec8d-106">取得遷移專案的方法。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="1ec8d-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ec8d-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec8d-108">範例1：取得</span><span class="sxs-lookup"><span data-stu-id="1ec8d-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="1ec8d-109">取得遷移專案的方法。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="1ec8d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ec8d-110">PARAMETERS</span></span>

### <span data-ttu-id="1ec8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec8d-111">-DefaultProfile</span></span>
<span data-ttu-id="1ec8d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec8d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ec8d-113">-Name</span></span>
<span data-ttu-id="1ec8d-114">Azure 遷移專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="1ec8d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec8d-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ec8d-116">遷移專案所屬之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="1ec8d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ec8d-117">-SubscriptionId</span></span>
<span data-ttu-id="1ec8d-118">在其中建立 [遷移] 專案的 Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1ec8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec8d-119">CommonParameters</span></span>
<span data-ttu-id="1ec8d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec8d-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec8d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1ec8d-122">INPUTS</span></span>

## <span data-ttu-id="1ec8d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1ec8d-123">OUTPUTS</span></span>

### <span data-ttu-id="1ec8d-124">IMigrateProject 中的 Api20180901Preview （）。</span><span class="sxs-lookup"><span data-stu-id="1ec8d-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="1ec8d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1ec8d-125">NOTES</span></span>

<span data-ttu-id="1ec8d-126">別名</span><span class="sxs-lookup"><span data-stu-id="1ec8d-126">ALIASES</span></span>

## <span data-ttu-id="1ec8d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ec8d-127">RELATED LINKS</span></span>

