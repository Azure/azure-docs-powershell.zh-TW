---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: b00010096b39cd714f01f33012309f8528a5ae3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909622"
---
# <span data-ttu-id="17c68-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="17c68-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="17c68-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17c68-102">SYNOPSIS</span></span>
<span data-ttu-id="17c68-103">取得網站的方法。</span><span class="sxs-lookup"><span data-stu-id="17c68-103">Method to get a site.</span></span>

## <span data-ttu-id="17c68-104">語法</span><span class="sxs-lookup"><span data-stu-id="17c68-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="17c68-105">描述</span><span class="sxs-lookup"><span data-stu-id="17c68-105">DESCRIPTION</span></span>
<span data-ttu-id="17c68-106">取得網站的方法。</span><span class="sxs-lookup"><span data-stu-id="17c68-106">Method to get a site.</span></span>

## <span data-ttu-id="17c68-107">例子</span><span class="sxs-lookup"><span data-stu-id="17c68-107">EXAMPLES</span></span>

### <span data-ttu-id="17c68-108">範例 1：取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="17c68-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="17c68-109">根據名稱取得網站</span><span class="sxs-lookup"><span data-stu-id="17c68-109">Get site by name</span></span>

## <span data-ttu-id="17c68-110">參數</span><span class="sxs-lookup"><span data-stu-id="17c68-110">PARAMETERS</span></span>

### <span data-ttu-id="17c68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c68-111">-DefaultProfile</span></span>
<span data-ttu-id="17c68-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17c68-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17c68-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="17c68-113">-Name</span></span>
<span data-ttu-id="17c68-114">網站名稱。</span><span class="sxs-lookup"><span data-stu-id="17c68-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c68-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c68-115">-ResourceGroupName</span></span>
<span data-ttu-id="17c68-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17c68-116">The name of the resource group.</span></span>
<span data-ttu-id="17c68-117">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="17c68-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="17c68-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17c68-118">-SubscriptionId</span></span>
<span data-ttu-id="17c68-119">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="17c68-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="17c68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c68-120">CommonParameters</span></span>
<span data-ttu-id="17c68-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17c68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c68-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17c68-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c68-123">輸入</span><span class="sxs-lookup"><span data-stu-id="17c68-123">INPUTS</span></span>

## <span data-ttu-id="17c68-124">輸出</span><span class="sxs-lookup"><span data-stu-id="17c68-124">OUTPUTS</span></span>

### <span data-ttu-id="17c68-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVVtsite</span><span class="sxs-lookup"><span data-stu-id="17c68-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="17c68-126">筆記</span><span class="sxs-lookup"><span data-stu-id="17c68-126">NOTES</span></span>

<span data-ttu-id="17c68-127">別名</span><span class="sxs-lookup"><span data-stu-id="17c68-127">ALIASES</span></span>

## <span data-ttu-id="17c68-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="17c68-128">RELATED LINKS</span></span>

