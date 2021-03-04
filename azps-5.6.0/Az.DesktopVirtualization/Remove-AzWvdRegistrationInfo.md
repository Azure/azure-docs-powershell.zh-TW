---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: 548e7d19e2d5285ed4063bc9c14202980c02028d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909054"
---
# <span data-ttu-id="d39a1-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="d39a1-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="d39a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d39a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d39a1-103">移除 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="d39a1-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d39a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="d39a1-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d39a1-105">描述</span><span class="sxs-lookup"><span data-stu-id="d39a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d39a1-106">移除 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="d39a1-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d39a1-107">例子</span><span class="sxs-lookup"><span data-stu-id="d39a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d39a1-108">範例 1：刪除 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="d39a1-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="d39a1-109">此命令會刪除主機集中的 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="d39a1-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="d39a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d39a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d39a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39a1-111">-DefaultProfile</span></span>
<span data-ttu-id="d39a1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d39a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d39a1-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d39a1-113">-HostPoolName</span></span>
<span data-ttu-id="d39a1-114">主機名稱</span><span class="sxs-lookup"><span data-stu-id="d39a1-114">Host Pool Name</span></span>

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

### <span data-ttu-id="d39a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="d39a1-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="d39a1-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d39a1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d39a1-117">-SubscriptionId</span></span>
<span data-ttu-id="d39a1-118">help foo 1</span><span class="sxs-lookup"><span data-stu-id="d39a1-118">help foo 1</span></span>

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

### <span data-ttu-id="d39a1-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d39a1-119">-Confirm</span></span>
<span data-ttu-id="d39a1-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d39a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39a1-121">-WhatIf</span></span>
<span data-ttu-id="d39a1-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d39a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d39a1-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d39a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39a1-124">CommonParameters</span></span>
<span data-ttu-id="d39a1-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d39a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39a1-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d39a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39a1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d39a1-127">INPUTS</span></span>

## <span data-ttu-id="d39a1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d39a1-128">OUTPUTS</span></span>

## <span data-ttu-id="d39a1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d39a1-129">NOTES</span></span>

<span data-ttu-id="d39a1-130">別名</span><span class="sxs-lookup"><span data-stu-id="d39a1-130">ALIASES</span></span>

## <span data-ttu-id="d39a1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d39a1-131">RELATED LINKS</span></span>

