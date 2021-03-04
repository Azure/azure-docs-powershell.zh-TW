---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: ef1829dec7bdc1c3b41fa9e418246e1d9afcc1f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905437"
---
# <span data-ttu-id="58d2d-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="58d2d-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="58d2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="58d2d-103">註冊 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="58d2d-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="58d2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="58d2d-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="58d2d-105">描述</span><span class="sxs-lookup"><span data-stu-id="58d2d-105">DESCRIPTION</span></span>
<span data-ttu-id="58d2d-106">註冊 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="58d2d-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="58d2d-107">例子</span><span class="sxs-lookup"><span data-stu-id="58d2d-107">EXAMPLES</span></span>

### <span data-ttu-id="58d2d-108">範例 1：註冊 Windows 虛擬桌面應用程式群組</span><span class="sxs-lookup"><span data-stu-id="58d2d-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="58d2d-109">此命令會向工作區登錄 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="58d2d-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="58d2d-110">參數</span><span class="sxs-lookup"><span data-stu-id="58d2d-110">PARAMETERS</span></span>

### <span data-ttu-id="58d2d-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="58d2d-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="58d2d-112">ApplicationGroupPath 路徑</span><span class="sxs-lookup"><span data-stu-id="58d2d-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="58d2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d2d-113">-DefaultProfile</span></span>
<span data-ttu-id="58d2d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58d2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d2d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d2d-115">-ResourceGroupName</span></span>
<span data-ttu-id="58d2d-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="58d2d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="58d2d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58d2d-117">-SubscriptionId</span></span>
<span data-ttu-id="58d2d-118">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="58d2d-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d2d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58d2d-119">-WorkspaceName</span></span>
<span data-ttu-id="58d2d-120">工作區名稱</span><span class="sxs-lookup"><span data-stu-id="58d2d-120">Workspace Name</span></span>

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

### <span data-ttu-id="58d2d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="58d2d-121">-Confirm</span></span>
<span data-ttu-id="58d2d-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58d2d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d2d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d2d-123">-WhatIf</span></span>
<span data-ttu-id="58d2d-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58d2d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d2d-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58d2d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d2d-126">CommonParameters</span></span>
<span data-ttu-id="58d2d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58d2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d2d-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58d2d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d2d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="58d2d-129">INPUTS</span></span>

## <span data-ttu-id="58d2d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="58d2d-130">OUTPUTS</span></span>

### <span data-ttu-id="58d2d-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="58d2d-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="58d2d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="58d2d-132">NOTES</span></span>

<span data-ttu-id="58d2d-133">別名</span><span class="sxs-lookup"><span data-stu-id="58d2d-133">ALIASES</span></span>

## <span data-ttu-id="58d2d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="58d2d-134">RELATED LINKS</span></span>

