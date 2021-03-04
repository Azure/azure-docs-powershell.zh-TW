---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909062"
---
# <span data-ttu-id="44bdc-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="44bdc-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="44bdc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="44bdc-103">列出給定應用程式群組中的開始功能表項目。</span><span class="sxs-lookup"><span data-stu-id="44bdc-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="44bdc-104">語法</span><span class="sxs-lookup"><span data-stu-id="44bdc-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="44bdc-105">描述</span><span class="sxs-lookup"><span data-stu-id="44bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="44bdc-106">列出給定應用程式群組中的開始功能表項目。</span><span class="sxs-lookup"><span data-stu-id="44bdc-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="44bdc-107">例子</span><span class="sxs-lookup"><span data-stu-id="44bdc-107">EXAMPLES</span></span>

### <span data-ttu-id="44bdc-108">範例 2：列出 Windows 虛擬桌面開始功能表項目</span><span class="sxs-lookup"><span data-stu-id="44bdc-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="44bdc-109">此命令會列出應用程式群組中的 Windows 虛擬桌面開始功能表項目。</span><span class="sxs-lookup"><span data-stu-id="44bdc-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="44bdc-110">參數</span><span class="sxs-lookup"><span data-stu-id="44bdc-110">PARAMETERS</span></span>

### <span data-ttu-id="44bdc-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="44bdc-111">-ApplicationGroupName</span></span>
<span data-ttu-id="44bdc-112">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="44bdc-112">The name of the application group</span></span>

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

### <span data-ttu-id="44bdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bdc-113">-DefaultProfile</span></span>
<span data-ttu-id="44bdc-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44bdc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44bdc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44bdc-115">-ResourceGroupName</span></span>
<span data-ttu-id="44bdc-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="44bdc-116">The name of the resource group.</span></span>
<span data-ttu-id="44bdc-117">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="44bdc-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44bdc-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44bdc-118">-SubscriptionId</span></span>
<span data-ttu-id="44bdc-119">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="44bdc-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="44bdc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bdc-120">CommonParameters</span></span>
<span data-ttu-id="44bdc-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44bdc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bdc-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44bdc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bdc-123">輸入</span><span class="sxs-lookup"><span data-stu-id="44bdc-123">INPUTS</span></span>

## <span data-ttu-id="44bdc-124">輸出</span><span class="sxs-lookup"><span data-stu-id="44bdc-124">OUTPUTS</span></span>

### <span data-ttu-id="44bdc-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="44bdc-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="44bdc-126">筆記</span><span class="sxs-lookup"><span data-stu-id="44bdc-126">NOTES</span></span>

<span data-ttu-id="44bdc-127">別名</span><span class="sxs-lookup"><span data-stu-id="44bdc-127">ALIASES</span></span>

## <span data-ttu-id="44bdc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="44bdc-128">RELATED LINKS</span></span>

