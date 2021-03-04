---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: d028e66fc5f1f4b2c3ab520bd76615e8e9e79099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909626"
---
# <span data-ttu-id="cc028-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="cc028-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="cc028-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc028-102">SYNOPSIS</span></span>
<span data-ttu-id="cc028-103">以帳戶方式執行的方法。</span><span class="sxs-lookup"><span data-stu-id="cc028-103">Method to get run as account.</span></span>

## <span data-ttu-id="cc028-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc028-104">SYNTAX</span></span>

### <span data-ttu-id="cc028-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="cc028-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc028-106">獲取</span><span class="sxs-lookup"><span data-stu-id="cc028-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cc028-107">描述</span><span class="sxs-lookup"><span data-stu-id="cc028-107">DESCRIPTION</span></span>
<span data-ttu-id="cc028-108">以帳戶方式執行的方法。</span><span class="sxs-lookup"><span data-stu-id="cc028-108">Method to get run as account.</span></span>

## <span data-ttu-id="cc028-109">例子</span><span class="sxs-lookup"><span data-stu-id="cc028-109">EXAMPLES</span></span>

### <span data-ttu-id="cc028-110">範例 1：清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="cc028-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="cc028-111">清單中所有專案會以帳戶在網站中執行。</span><span class="sxs-lookup"><span data-stu-id="cc028-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="cc028-112">範例 2：取得</span><span class="sxs-lookup"><span data-stu-id="cc028-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="cc028-113">以帳戶名稱取得執行。</span><span class="sxs-lookup"><span data-stu-id="cc028-113">Get Run as account by name.</span></span>

## <span data-ttu-id="cc028-114">參數</span><span class="sxs-lookup"><span data-stu-id="cc028-114">PARAMETERS</span></span>

### <span data-ttu-id="cc028-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cc028-115">-AccountName</span></span>
<span data-ttu-id="cc028-116">以帳戶 ARM 名稱執行。</span><span class="sxs-lookup"><span data-stu-id="cc028-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="cc028-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc028-117">-DefaultProfile</span></span>
<span data-ttu-id="cc028-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc028-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc028-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc028-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc028-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc028-120">The name of the resource group.</span></span>
<span data-ttu-id="cc028-121">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cc028-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cc028-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="cc028-122">-SiteName</span></span>
<span data-ttu-id="cc028-123">網站名稱。</span><span class="sxs-lookup"><span data-stu-id="cc028-123">Site name.</span></span>

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

### <span data-ttu-id="cc028-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc028-124">-SubscriptionId</span></span>
<span data-ttu-id="cc028-125">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc028-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cc028-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc028-126">CommonParameters</span></span>
<span data-ttu-id="cc028-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc028-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc028-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc028-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc028-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cc028-129">INPUTS</span></span>

## <span data-ttu-id="cc028-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cc028-130">OUTPUTS</span></span>

### <span data-ttu-id="cc028-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVSoftRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="cc028-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="cc028-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cc028-132">NOTES</span></span>

<span data-ttu-id="cc028-133">別名</span><span class="sxs-lookup"><span data-stu-id="cc028-133">ALIASES</span></span>

## <span data-ttu-id="cc028-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc028-134">RELATED LINKS</span></span>

