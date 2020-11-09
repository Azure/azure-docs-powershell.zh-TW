---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284760"
---
# <span data-ttu-id="9aa67-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="9aa67-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="9aa67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9aa67-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa67-103">清單中的 [開始] 功能表項目目在指定的應用程式群組中。</span><span class="sxs-lookup"><span data-stu-id="9aa67-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="9aa67-104">句法</span><span class="sxs-lookup"><span data-stu-id="9aa67-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9aa67-105">說明</span><span class="sxs-lookup"><span data-stu-id="9aa67-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa67-106">清單中的 [開始] 功能表項目目在指定的應用程式群組中。</span><span class="sxs-lookup"><span data-stu-id="9aa67-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="9aa67-107">示例</span><span class="sxs-lookup"><span data-stu-id="9aa67-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa67-108">範例2：列出 Windows 虛擬桌面 [開始] 功能表項目目</span><span class="sxs-lookup"><span data-stu-id="9aa67-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="9aa67-109">這個命令會列出 [applicaton] 群組中的 Windows 虛擬桌面 [開始] 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="9aa67-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="9aa67-110">參數</span><span class="sxs-lookup"><span data-stu-id="9aa67-110">PARAMETERS</span></span>

### <span data-ttu-id="9aa67-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa67-111">-ApplicationGroupName</span></span>
<span data-ttu-id="9aa67-112">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9aa67-112">The name of the application group</span></span>

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

### <span data-ttu-id="9aa67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa67-113">-DefaultProfile</span></span>
<span data-ttu-id="9aa67-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9aa67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa67-115">-ResourceGroupName</span></span>
<span data-ttu-id="9aa67-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa67-116">The name of the resource group.</span></span>
<span data-ttu-id="9aa67-117">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9aa67-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9aa67-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9aa67-118">-SubscriptionId</span></span>
<span data-ttu-id="9aa67-119">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="9aa67-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9aa67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa67-120">CommonParameters</span></span>
<span data-ttu-id="9aa67-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9aa67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa67-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9aa67-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa67-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9aa67-123">INPUTS</span></span>

## <span data-ttu-id="9aa67-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9aa67-124">OUTPUTS</span></span>

### <span data-ttu-id="9aa67-125">IStartMenuItem （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="9aa67-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="9aa67-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9aa67-126">NOTES</span></span>

<span data-ttu-id="9aa67-127">別名</span><span class="sxs-lookup"><span data-stu-id="9aa67-127">ALIASES</span></span>

## <span data-ttu-id="9aa67-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9aa67-128">RELATED LINKS</span></span>

