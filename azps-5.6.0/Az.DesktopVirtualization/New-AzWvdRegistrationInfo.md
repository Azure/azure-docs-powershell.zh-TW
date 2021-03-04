---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 7e633d2ba607132de6dbdfc262642659cc5e4c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905449"
---
# <span data-ttu-id="effd6-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="effd6-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="effd6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="effd6-102">SYNOPSIS</span></span>
<span data-ttu-id="effd6-103">建立 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="effd6-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="effd6-104">語法</span><span class="sxs-lookup"><span data-stu-id="effd6-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="effd6-105">描述</span><span class="sxs-lookup"><span data-stu-id="effd6-105">DESCRIPTION</span></span>
<span data-ttu-id="effd6-106">建立 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="effd6-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="effd6-107">例子</span><span class="sxs-lookup"><span data-stu-id="effd6-107">EXAMPLES</span></span>

### <span data-ttu-id="effd6-108">範例 1：建立 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="effd6-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="effd6-109">此命令在主機集中建立 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="effd6-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="effd6-110">參數</span><span class="sxs-lookup"><span data-stu-id="effd6-110">PARAMETERS</span></span>

### <span data-ttu-id="effd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="effd6-111">-DefaultProfile</span></span>
<span data-ttu-id="effd6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="effd6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="effd6-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="effd6-113">-ExpirationTime</span></span>
<span data-ttu-id="effd6-114">到期日</span><span class="sxs-lookup"><span data-stu-id="effd6-114">Expiration Time</span></span>

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

### <span data-ttu-id="effd6-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="effd6-115">-HostPoolName</span></span>
<span data-ttu-id="effd6-116">主機名稱</span><span class="sxs-lookup"><span data-stu-id="effd6-116">Host Pool Name</span></span>

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

### <span data-ttu-id="effd6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="effd6-117">-ResourceGroupName</span></span>
<span data-ttu-id="effd6-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="effd6-118">Resource Group Name</span></span>

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

### <span data-ttu-id="effd6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="effd6-119">-SubscriptionId</span></span>
<span data-ttu-id="effd6-120">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="effd6-120">Subscription Id</span></span>

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

### <span data-ttu-id="effd6-121">-確認</span><span class="sxs-lookup"><span data-stu-id="effd6-121">-Confirm</span></span>
<span data-ttu-id="effd6-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="effd6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="effd6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="effd6-123">-WhatIf</span></span>
<span data-ttu-id="effd6-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="effd6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="effd6-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="effd6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="effd6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="effd6-126">CommonParameters</span></span>
<span data-ttu-id="effd6-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="effd6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="effd6-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="effd6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="effd6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="effd6-129">INPUTS</span></span>

## <span data-ttu-id="effd6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="effd6-130">OUTPUTS</span></span>

### <span data-ttu-id="effd6-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="effd6-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="effd6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="effd6-132">NOTES</span></span>

<span data-ttu-id="effd6-133">別名</span><span class="sxs-lookup"><span data-stu-id="effd6-133">ALIASES</span></span>

## <span data-ttu-id="effd6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="effd6-134">RELATED LINKS</span></span>

