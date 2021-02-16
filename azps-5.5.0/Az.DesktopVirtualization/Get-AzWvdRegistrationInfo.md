---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139267"
---
# <span data-ttu-id="4896a-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4896a-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="4896a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4896a-102">SYNOPSIS</span></span>
<span data-ttu-id="4896a-103">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="4896a-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4896a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4896a-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4896a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4896a-105">DESCRIPTION</span></span>
<span data-ttu-id="4896a-106">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="4896a-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4896a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4896a-107">EXAMPLES</span></span>

### <span data-ttu-id="4896a-108">範例1：取得 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="4896a-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="4896a-109">這個命令會在主機池中取得 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="4896a-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="4896a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4896a-110">PARAMETERS</span></span>

### <span data-ttu-id="4896a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4896a-111">-DefaultProfile</span></span>
<span data-ttu-id="4896a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4896a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4896a-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4896a-113">-HostPoolName</span></span>
<span data-ttu-id="4896a-114">主機池名稱</span><span class="sxs-lookup"><span data-stu-id="4896a-114">Host Pool Name</span></span>

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

### <span data-ttu-id="4896a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4896a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4896a-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4896a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4896a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4896a-117">-SubscriptionId</span></span>
<span data-ttu-id="4896a-118">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="4896a-118">Subscription Id</span></span>

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

### <span data-ttu-id="4896a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4896a-119">CommonParameters</span></span>
<span data-ttu-id="4896a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4896a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4896a-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4896a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4896a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4896a-122">INPUTS</span></span>

## <span data-ttu-id="4896a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4896a-123">OUTPUTS</span></span>

### <span data-ttu-id="4896a-124">RegistrationInfo （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="4896a-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="4896a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4896a-125">NOTES</span></span>

<span data-ttu-id="4896a-126">別名</span><span class="sxs-lookup"><span data-stu-id="4896a-126">ALIASES</span></span>

## <span data-ttu-id="4896a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4896a-127">RELATED LINKS</span></span>

