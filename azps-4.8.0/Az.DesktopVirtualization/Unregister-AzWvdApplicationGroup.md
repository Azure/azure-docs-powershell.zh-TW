---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136448"
---
# <span data-ttu-id="b5cd4-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="b5cd4-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="b5cd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="b5cd4-103">取消註冊 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="b5cd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5cd4-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b5cd4-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="b5cd4-106">取消註冊 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="b5cd4-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5cd4-107">EXAMPLES</span></span>

### <span data-ttu-id="b5cd4-108">範例1：取消註冊 Windows 虛擬桌面應用程式群組</span><span class="sxs-lookup"><span data-stu-id="b5cd4-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="b5cd4-109">這個命令會將 Windows 虛擬桌面應用程式群組取消註冊至工作區。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="b5cd4-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5cd4-110">PARAMETERS</span></span>

### <span data-ttu-id="b5cd4-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="b5cd4-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="b5cd4-112">ResourceGroupName 路徑</span><span class="sxs-lookup"><span data-stu-id="b5cd4-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="b5cd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5cd4-113">-DefaultProfile</span></span>
<span data-ttu-id="b5cd4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5cd4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5cd4-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5cd4-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b5cd4-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b5cd4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5cd4-117">-SubscriptionId</span></span>
<span data-ttu-id="b5cd4-118">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="b5cd4-118">Subscription Id</span></span>

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

### <span data-ttu-id="b5cd4-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5cd4-119">-WorkspaceName</span></span>
<span data-ttu-id="b5cd4-120">工作區名稱</span><span class="sxs-lookup"><span data-stu-id="b5cd4-120">Workspace Name</span></span>

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

### <span data-ttu-id="b5cd4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b5cd4-121">-Confirm</span></span>
<span data-ttu-id="b5cd4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5cd4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5cd4-123">-WhatIf</span></span>
<span data-ttu-id="b5cd4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5cd4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5cd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5cd4-126">CommonParameters</span></span>
<span data-ttu-id="b5cd4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5cd4-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5cd4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b5cd4-129">INPUTS</span></span>

## <span data-ttu-id="b5cd4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b5cd4-130">OUTPUTS</span></span>

### <span data-ttu-id="b5cd4-131">IWorkspace （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="b5cd4-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="b5cd4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b5cd4-132">NOTES</span></span>

<span data-ttu-id="b5cd4-133">別名</span><span class="sxs-lookup"><span data-stu-id="b5cd4-133">ALIASES</span></span>

## <span data-ttu-id="b5cd4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5cd4-134">RELATED LINKS</span></span>

