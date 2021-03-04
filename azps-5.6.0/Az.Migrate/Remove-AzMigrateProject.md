---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: d9edb00bf7944400fa681f857dd7005d9eaf69b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915393"
---
# <span data-ttu-id="4bd80-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="4bd80-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="4bd80-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4bd80-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd80-103">刪除遷移專案。</span><span class="sxs-lookup"><span data-stu-id="4bd80-103">Delete the migrate project.</span></span>
<span data-ttu-id="4bd80-104">刪除不存在的專案是一項沒有作業的專案。</span><span class="sxs-lookup"><span data-stu-id="4bd80-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="4bd80-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bd80-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bd80-106">描述</span><span class="sxs-lookup"><span data-stu-id="4bd80-106">DESCRIPTION</span></span>
<span data-ttu-id="4bd80-107">刪除遷移專案。</span><span class="sxs-lookup"><span data-stu-id="4bd80-107">Delete the migrate project.</span></span>
<span data-ttu-id="4bd80-108">刪除不存在的專案是一項沒有作業的專案。</span><span class="sxs-lookup"><span data-stu-id="4bd80-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="4bd80-109">例子</span><span class="sxs-lookup"><span data-stu-id="4bd80-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd80-110">範例 1：刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="4bd80-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="4bd80-111">刪除遷移專案。</span><span class="sxs-lookup"><span data-stu-id="4bd80-111">Delete the migrate project.</span></span>
<span data-ttu-id="4bd80-112">刪除不存在的專案是一項沒有作業的專案。</span><span class="sxs-lookup"><span data-stu-id="4bd80-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="4bd80-113">參數</span><span class="sxs-lookup"><span data-stu-id="4bd80-113">PARAMETERS</span></span>

### <span data-ttu-id="4bd80-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4bd80-114">-AcceptLanguage</span></span>
<span data-ttu-id="4bd80-115">標準要求標題。</span><span class="sxs-lookup"><span data-stu-id="4bd80-115">Standard request header.</span></span>
<span data-ttu-id="4bd80-116">服務用來以適當的語言回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="4bd80-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="4bd80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd80-117">-DefaultProfile</span></span>
<span data-ttu-id="4bd80-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bd80-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd80-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bd80-119">-Name</span></span>
<span data-ttu-id="4bd80-120">Azure Migrate 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd80-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="4bd80-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bd80-121">-PassThru</span></span>
<span data-ttu-id="4bd80-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4bd80-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4bd80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd80-123">-ResourceGroupName</span></span>
<span data-ttu-id="4bd80-124">其中一部分是要遷移專案的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="4bd80-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="4bd80-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bd80-125">-SubscriptionId</span></span>
<span data-ttu-id="4bd80-126">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4bd80-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="4bd80-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4bd80-127">-Confirm</span></span>
<span data-ttu-id="4bd80-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4bd80-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bd80-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd80-129">-WhatIf</span></span>
<span data-ttu-id="4bd80-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bd80-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd80-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bd80-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bd80-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd80-132">CommonParameters</span></span>
<span data-ttu-id="4bd80-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4bd80-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd80-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bd80-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd80-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4bd80-135">INPUTS</span></span>

## <span data-ttu-id="4bd80-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4bd80-136">OUTPUTS</span></span>

### <span data-ttu-id="4bd80-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4bd80-137">System.Boolean</span></span>

## <span data-ttu-id="4bd80-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4bd80-138">NOTES</span></span>

<span data-ttu-id="4bd80-139">別名</span><span class="sxs-lookup"><span data-stu-id="4bd80-139">ALIASES</span></span>

## <span data-ttu-id="4bd80-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bd80-140">RELATED LINKS</span></span>

