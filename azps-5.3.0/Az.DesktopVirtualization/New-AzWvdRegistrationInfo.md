---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289231"
---
# <span data-ttu-id="72663-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="72663-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="72663-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72663-102">SYNOPSIS</span></span>
<span data-ttu-id="72663-103">建立 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="72663-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="72663-104">句法</span><span class="sxs-lookup"><span data-stu-id="72663-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72663-105">說明</span><span class="sxs-lookup"><span data-stu-id="72663-105">DESCRIPTION</span></span>
<span data-ttu-id="72663-106">建立 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="72663-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="72663-107">示例</span><span class="sxs-lookup"><span data-stu-id="72663-107">EXAMPLES</span></span>

### <span data-ttu-id="72663-108">範例1：建立 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="72663-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="72663-109">這個命令會在主機池中建立 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="72663-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="72663-110">參數</span><span class="sxs-lookup"><span data-stu-id="72663-110">PARAMETERS</span></span>

### <span data-ttu-id="72663-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72663-111">-DefaultProfile</span></span>
<span data-ttu-id="72663-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72663-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72663-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="72663-113">-ExpirationTime</span></span>
<span data-ttu-id="72663-114">到期時間</span><span class="sxs-lookup"><span data-stu-id="72663-114">Expiration Time</span></span>

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

### <span data-ttu-id="72663-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="72663-115">-HostPoolName</span></span>
<span data-ttu-id="72663-116">主機池名稱</span><span class="sxs-lookup"><span data-stu-id="72663-116">Host Pool Name</span></span>

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

### <span data-ttu-id="72663-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72663-117">-ResourceGroupName</span></span>
<span data-ttu-id="72663-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="72663-118">Resource Group Name</span></span>

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

### <span data-ttu-id="72663-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72663-119">-SubscriptionId</span></span>
<span data-ttu-id="72663-120">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="72663-120">Subscription Id</span></span>

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

### <span data-ttu-id="72663-121">-確認</span><span class="sxs-lookup"><span data-stu-id="72663-121">-Confirm</span></span>
<span data-ttu-id="72663-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72663-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72663-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72663-123">-WhatIf</span></span>
<span data-ttu-id="72663-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72663-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72663-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72663-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72663-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72663-126">CommonParameters</span></span>
<span data-ttu-id="72663-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72663-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72663-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="72663-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72663-129">輸入</span><span class="sxs-lookup"><span data-stu-id="72663-129">INPUTS</span></span>

## <span data-ttu-id="72663-130">輸出</span><span class="sxs-lookup"><span data-stu-id="72663-130">OUTPUTS</span></span>

### <span data-ttu-id="72663-131">IRegistrationInfo （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="72663-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="72663-132">筆記</span><span class="sxs-lookup"><span data-stu-id="72663-132">NOTES</span></span>

<span data-ttu-id="72663-133">別名</span><span class="sxs-lookup"><span data-stu-id="72663-133">ALIASES</span></span>

## <span data-ttu-id="72663-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="72663-134">RELATED LINKS</span></span>

