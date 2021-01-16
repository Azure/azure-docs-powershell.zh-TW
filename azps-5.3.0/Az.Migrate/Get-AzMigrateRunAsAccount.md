---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435315"
---
# <span data-ttu-id="13483-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="13483-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="13483-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13483-102">SYNOPSIS</span></span>
<span data-ttu-id="13483-103">取得 [執行方式] 帳戶的方法。</span><span class="sxs-lookup"><span data-stu-id="13483-103">Method to get run as account.</span></span>

## <span data-ttu-id="13483-104">句法</span><span class="sxs-lookup"><span data-stu-id="13483-104">SYNTAX</span></span>

### <span data-ttu-id="13483-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="13483-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13483-106">獲取</span><span class="sxs-lookup"><span data-stu-id="13483-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="13483-107">說明</span><span class="sxs-lookup"><span data-stu-id="13483-107">DESCRIPTION</span></span>
<span data-ttu-id="13483-108">取得 [執行方式] 帳戶的方法。</span><span class="sxs-lookup"><span data-stu-id="13483-108">Method to get run as account.</span></span>

## <span data-ttu-id="13483-109">示例</span><span class="sxs-lookup"><span data-stu-id="13483-109">EXAMPLES</span></span>

### <span data-ttu-id="13483-110">範例1： (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="13483-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="13483-111">清單網站中的所有執行方式帳戶。</span><span class="sxs-lookup"><span data-stu-id="13483-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="13483-112">範例2：取得</span><span class="sxs-lookup"><span data-stu-id="13483-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="13483-113">透過名稱取得 [執行方式] 帳戶。</span><span class="sxs-lookup"><span data-stu-id="13483-113">Get Run as account by name.</span></span>

## <span data-ttu-id="13483-114">參數</span><span class="sxs-lookup"><span data-stu-id="13483-114">PARAMETERS</span></span>

### <span data-ttu-id="13483-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13483-115">-AccountName</span></span>
<span data-ttu-id="13483-116">執行方式帳戶 ARM 名稱。</span><span class="sxs-lookup"><span data-stu-id="13483-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13483-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13483-117">-DefaultProfile</span></span>
<span data-ttu-id="13483-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13483-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13483-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13483-119">-ResourceGroupName</span></span>
<span data-ttu-id="13483-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13483-120">The name of the resource group.</span></span>
<span data-ttu-id="13483-121">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="13483-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="13483-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="13483-122">-SiteName</span></span>
<span data-ttu-id="13483-123">網站名稱。</span><span class="sxs-lookup"><span data-stu-id="13483-123">Site name.</span></span>

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

### <span data-ttu-id="13483-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13483-124">-SubscriptionId</span></span>
<span data-ttu-id="13483-125">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="13483-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="13483-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13483-126">CommonParameters</span></span>
<span data-ttu-id="13483-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13483-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13483-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13483-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13483-129">輸入</span><span class="sxs-lookup"><span data-stu-id="13483-129">INPUTS</span></span>

## <span data-ttu-id="13483-130">輸出</span><span class="sxs-lookup"><span data-stu-id="13483-130">OUTPUTS</span></span>

### <span data-ttu-id="13483-131">IVMwareRunAsAccount 中的 Api202001 （）。</span><span class="sxs-lookup"><span data-stu-id="13483-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="13483-132">筆記</span><span class="sxs-lookup"><span data-stu-id="13483-132">NOTES</span></span>

<span data-ttu-id="13483-133">別名</span><span class="sxs-lookup"><span data-stu-id="13483-133">ALIASES</span></span>

## <span data-ttu-id="13483-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="13483-134">RELATED LINKS</span></span>

