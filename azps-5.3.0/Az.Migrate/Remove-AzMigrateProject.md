---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435312"
---
# <span data-ttu-id="e2fb7-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="e2fb7-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="e2fb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fb7-103">刪除 [遷移專案]。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-103">Delete the migrate project.</span></span>
<span data-ttu-id="e2fb7-104">刪除不存在的專案是無操作。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e2fb7-105">句法</span><span class="sxs-lookup"><span data-stu-id="e2fb7-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2fb7-106">說明</span><span class="sxs-lookup"><span data-stu-id="e2fb7-106">DESCRIPTION</span></span>
<span data-ttu-id="e2fb7-107">刪除 [遷移專案]。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-107">Delete the migrate project.</span></span>
<span data-ttu-id="e2fb7-108">刪除不存在的專案是無操作。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e2fb7-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2fb7-109">EXAMPLES</span></span>

### <span data-ttu-id="e2fb7-110">範例1：刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e2fb7-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="e2fb7-111">刪除 [遷移專案]。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-111">Delete the migrate project.</span></span>
<span data-ttu-id="e2fb7-112">刪除不存在的專案是無操作。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e2fb7-113">參數</span><span class="sxs-lookup"><span data-stu-id="e2fb7-113">PARAMETERS</span></span>

### <span data-ttu-id="e2fb7-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e2fb7-114">-AcceptLanguage</span></span>
<span data-ttu-id="e2fb7-115">標準要求標頭。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-115">Standard request header.</span></span>
<span data-ttu-id="e2fb7-116">由服務用來以適當的語言回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-116">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fb7-117">-DefaultProfile</span></span>
<span data-ttu-id="e2fb7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2fb7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2fb7-119">-Name</span></span>
<span data-ttu-id="e2fb7-120">Azure 遷移專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="e2fb7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2fb7-121">-PassThru</span></span>
<span data-ttu-id="e2fb7-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e2fb7-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2fb7-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2fb7-124">遷移專案所屬之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="e2fb7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2fb7-125">-SubscriptionId</span></span>
<span data-ttu-id="e2fb7-126">在其中建立 [遷移] 專案的 Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e2fb7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e2fb7-127">-Confirm</span></span>
<span data-ttu-id="e2fb7-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2fb7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2fb7-129">-WhatIf</span></span>
<span data-ttu-id="e2fb7-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2fb7-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2fb7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fb7-132">CommonParameters</span></span>
<span data-ttu-id="e2fb7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fb7-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2fb7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fb7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e2fb7-135">INPUTS</span></span>

## <span data-ttu-id="e2fb7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e2fb7-136">OUTPUTS</span></span>

### <span data-ttu-id="e2fb7-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e2fb7-137">System.Boolean</span></span>

## <span data-ttu-id="e2fb7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e2fb7-138">NOTES</span></span>

<span data-ttu-id="e2fb7-139">別名</span><span class="sxs-lookup"><span data-stu-id="e2fb7-139">ALIASES</span></span>

## <span data-ttu-id="e2fb7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2fb7-140">RELATED LINKS</span></span>

