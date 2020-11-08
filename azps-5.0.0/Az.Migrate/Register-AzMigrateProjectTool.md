---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140079"
---
# <span data-ttu-id="e3d53-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="e3d53-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="e3d53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3d53-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d53-103">使用 [遷移] 專案來註冊工具。</span><span class="sxs-lookup"><span data-stu-id="e3d53-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="e3d53-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3d53-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3d53-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3d53-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d53-106">使用 [遷移] 專案來註冊工具。</span><span class="sxs-lookup"><span data-stu-id="e3d53-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="e3d53-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3d53-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d53-108">範例1：註冊工具。</span><span class="sxs-lookup"><span data-stu-id="e3d53-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="e3d53-109">使用 [遷移] 專案來註冊工具。</span><span class="sxs-lookup"><span data-stu-id="e3d53-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="e3d53-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3d53-110">PARAMETERS</span></span>

### <span data-ttu-id="e3d53-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e3d53-111">-AcceptLanguage</span></span>
<span data-ttu-id="e3d53-112">標準要求標頭。</span><span class="sxs-lookup"><span data-stu-id="e3d53-112">Standard request header.</span></span>
<span data-ttu-id="e3d53-113">由服務用來以適當的語言回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="e3d53-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="e3d53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d53-114">-DefaultProfile</span></span>
<span data-ttu-id="e3d53-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3d53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d53-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="e3d53-116">-MigrateProjectName</span></span>
<span data-ttu-id="e3d53-117">Azure 遷移專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3d53-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="e3d53-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d53-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3d53-119">遷移專案所屬之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3d53-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="e3d53-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3d53-120">-SubscriptionId</span></span>
<span data-ttu-id="e3d53-121">在其中建立 [遷移] 專案的 Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="e3d53-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e3d53-122">-工具</span><span class="sxs-lookup"><span data-stu-id="e3d53-122">-Tool</span></span>
<span data-ttu-id="e3d53-123">取得或設定要註冊的工具。</span><span class="sxs-lookup"><span data-stu-id="e3d53-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="e3d53-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e3d53-124">-Confirm</span></span>
<span data-ttu-id="e3d53-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3d53-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d53-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d53-126">-WhatIf</span></span>
<span data-ttu-id="e3d53-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3d53-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d53-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3d53-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d53-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d53-129">CommonParameters</span></span>
<span data-ttu-id="e3d53-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3d53-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d53-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3d53-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d53-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e3d53-132">INPUTS</span></span>

## <span data-ttu-id="e3d53-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e3d53-133">OUTPUTS</span></span>

### <span data-ttu-id="e3d53-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e3d53-134">System.Boolean</span></span>

## <span data-ttu-id="e3d53-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e3d53-135">NOTES</span></span>

<span data-ttu-id="e3d53-136">別名</span><span class="sxs-lookup"><span data-stu-id="e3d53-136">ALIASES</span></span>

## <span data-ttu-id="e3d53-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3d53-137">RELATED LINKS</span></span>

