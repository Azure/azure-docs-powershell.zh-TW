---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140320"
---
# <span data-ttu-id="6bae1-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="6bae1-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="6bae1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bae1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bae1-103">取得網站的方法。</span><span class="sxs-lookup"><span data-stu-id="6bae1-103">Method to get a site.</span></span>

## <span data-ttu-id="6bae1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bae1-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6bae1-105">說明</span><span class="sxs-lookup"><span data-stu-id="6bae1-105">DESCRIPTION</span></span>
<span data-ttu-id="6bae1-106">取得網站的方法。</span><span class="sxs-lookup"><span data-stu-id="6bae1-106">Method to get a site.</span></span>

## <span data-ttu-id="6bae1-107">示例</span><span class="sxs-lookup"><span data-stu-id="6bae1-107">EXAMPLES</span></span>

### <span data-ttu-id="6bae1-108">範例1：取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="6bae1-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="6bae1-109">依名稱取得網站</span><span class="sxs-lookup"><span data-stu-id="6bae1-109">Get site by name</span></span>

## <span data-ttu-id="6bae1-110">參數</span><span class="sxs-lookup"><span data-stu-id="6bae1-110">PARAMETERS</span></span>

### <span data-ttu-id="6bae1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bae1-111">-DefaultProfile</span></span>
<span data-ttu-id="6bae1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bae1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bae1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bae1-113">-Name</span></span>
<span data-ttu-id="6bae1-114">網站名稱。</span><span class="sxs-lookup"><span data-stu-id="6bae1-114">Site name.</span></span>

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

### <span data-ttu-id="6bae1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bae1-115">-ResourceGroupName</span></span>
<span data-ttu-id="6bae1-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bae1-116">The name of the resource group.</span></span>
<span data-ttu-id="6bae1-117">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6bae1-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6bae1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bae1-118">-SubscriptionId</span></span>
<span data-ttu-id="6bae1-119">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="6bae1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6bae1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bae1-120">CommonParameters</span></span>
<span data-ttu-id="6bae1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bae1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bae1-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6bae1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bae1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6bae1-123">INPUTS</span></span>

## <span data-ttu-id="6bae1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6bae1-124">OUTPUTS</span></span>

### <span data-ttu-id="6bae1-125">IVMwareSite 中的 Api202001 （）。</span><span class="sxs-lookup"><span data-stu-id="6bae1-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="6bae1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6bae1-126">NOTES</span></span>

<span data-ttu-id="6bae1-127">別名</span><span class="sxs-lookup"><span data-stu-id="6bae1-127">ALIASES</span></span>

## <span data-ttu-id="6bae1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bae1-128">RELATED LINKS</span></span>

