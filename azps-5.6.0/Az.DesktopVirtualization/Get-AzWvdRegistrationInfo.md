---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 868cbf6aaaf9b9c304c6afa65e63e6eca12910d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904430"
---
# <span data-ttu-id="6db9e-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="6db9e-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="6db9e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6db9e-102">SYNOPSIS</span></span>
<span data-ttu-id="6db9e-103">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="6db9e-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="6db9e-104">語法</span><span class="sxs-lookup"><span data-stu-id="6db9e-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6db9e-105">描述</span><span class="sxs-lookup"><span data-stu-id="6db9e-105">DESCRIPTION</span></span>
<span data-ttu-id="6db9e-106">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="6db9e-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="6db9e-107">例子</span><span class="sxs-lookup"><span data-stu-id="6db9e-107">EXAMPLES</span></span>

### <span data-ttu-id="6db9e-108">範例 1：取得 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="6db9e-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="6db9e-109">此命令在主機集中會獲得 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="6db9e-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="6db9e-110">參數</span><span class="sxs-lookup"><span data-stu-id="6db9e-110">PARAMETERS</span></span>

### <span data-ttu-id="6db9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db9e-111">-DefaultProfile</span></span>
<span data-ttu-id="6db9e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6db9e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db9e-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6db9e-113">-HostPoolName</span></span>
<span data-ttu-id="6db9e-114">主機名稱</span><span class="sxs-lookup"><span data-stu-id="6db9e-114">Host Pool Name</span></span>

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

### <span data-ttu-id="6db9e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db9e-115">-ResourceGroupName</span></span>
<span data-ttu-id="6db9e-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="6db9e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6db9e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6db9e-117">-SubscriptionId</span></span>
<span data-ttu-id="6db9e-118">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="6db9e-118">Subscription Id</span></span>

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

### <span data-ttu-id="6db9e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db9e-119">CommonParameters</span></span>
<span data-ttu-id="6db9e-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6db9e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db9e-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6db9e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db9e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6db9e-122">INPUTS</span></span>

## <span data-ttu-id="6db9e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6db9e-123">OUTPUTS</span></span>

### <span data-ttu-id="6db9e-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="6db9e-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="6db9e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="6db9e-125">NOTES</span></span>

<span data-ttu-id="6db9e-126">別名</span><span class="sxs-lookup"><span data-stu-id="6db9e-126">ALIASES</span></span>

## <span data-ttu-id="6db9e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6db9e-127">RELATED LINKS</span></span>

