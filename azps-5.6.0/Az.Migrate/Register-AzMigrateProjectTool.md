---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: 60cc9b5b537c1d8e46f5bae56d93b33fa04f6c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908117"
---
# <span data-ttu-id="08329-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="08329-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="08329-102">簡介</span><span class="sxs-lookup"><span data-stu-id="08329-102">SYNOPSIS</span></span>
<span data-ttu-id="08329-103">向遷移專案註冊工具。</span><span class="sxs-lookup"><span data-stu-id="08329-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="08329-104">語法</span><span class="sxs-lookup"><span data-stu-id="08329-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08329-105">描述</span><span class="sxs-lookup"><span data-stu-id="08329-105">DESCRIPTION</span></span>
<span data-ttu-id="08329-106">向遷移專案註冊工具。</span><span class="sxs-lookup"><span data-stu-id="08329-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="08329-107">例子</span><span class="sxs-lookup"><span data-stu-id="08329-107">EXAMPLES</span></span>

### <span data-ttu-id="08329-108">範例 1：REgister 工具。</span><span class="sxs-lookup"><span data-stu-id="08329-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="08329-109">向遷移專案註冊工具。</span><span class="sxs-lookup"><span data-stu-id="08329-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="08329-110">參數</span><span class="sxs-lookup"><span data-stu-id="08329-110">PARAMETERS</span></span>

### <span data-ttu-id="08329-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="08329-111">-AcceptLanguage</span></span>
<span data-ttu-id="08329-112">標準要求標題。</span><span class="sxs-lookup"><span data-stu-id="08329-112">Standard request header.</span></span>
<span data-ttu-id="08329-113">服務用來以適當的語言回應用戶端。</span><span class="sxs-lookup"><span data-stu-id="08329-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="08329-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08329-114">-DefaultProfile</span></span>
<span data-ttu-id="08329-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="08329-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08329-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="08329-116">-MigrateProjectName</span></span>
<span data-ttu-id="08329-117">Azure Migrate 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="08329-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="08329-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08329-118">-ResourceGroupName</span></span>
<span data-ttu-id="08329-119">其中一部分是要遷移專案的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="08329-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="08329-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08329-120">-SubscriptionId</span></span>
<span data-ttu-id="08329-121">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="08329-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="08329-122">-工具</span><span class="sxs-lookup"><span data-stu-id="08329-122">-Tool</span></span>
<span data-ttu-id="08329-123">獲得或設定要登錄的工具。</span><span class="sxs-lookup"><span data-stu-id="08329-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="08329-124">-確認</span><span class="sxs-lookup"><span data-stu-id="08329-124">-Confirm</span></span>
<span data-ttu-id="08329-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="08329-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08329-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08329-126">-WhatIf</span></span>
<span data-ttu-id="08329-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08329-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08329-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08329-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08329-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08329-129">CommonParameters</span></span>
<span data-ttu-id="08329-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="08329-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08329-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08329-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08329-132">輸入</span><span class="sxs-lookup"><span data-stu-id="08329-132">INPUTS</span></span>

## <span data-ttu-id="08329-133">輸出</span><span class="sxs-lookup"><span data-stu-id="08329-133">OUTPUTS</span></span>

### <span data-ttu-id="08329-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="08329-134">System.Boolean</span></span>

## <span data-ttu-id="08329-135">筆記</span><span class="sxs-lookup"><span data-stu-id="08329-135">NOTES</span></span>

<span data-ttu-id="08329-136">別名</span><span class="sxs-lookup"><span data-stu-id="08329-136">ALIASES</span></span>

## <span data-ttu-id="08329-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="08329-137">RELATED LINKS</span></span>

