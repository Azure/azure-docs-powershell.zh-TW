---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 33e0b68e70cb65eee4e9e3178745645aafeb9f9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275531"
---
# <span data-ttu-id="df1b5-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="df1b5-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="df1b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="df1b5-103">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="df1b5-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="df1b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="df1b5-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="df1b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="df1b5-105">DESCRIPTION</span></span>
<span data-ttu-id="df1b5-106">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="df1b5-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="df1b5-107">示例</span><span class="sxs-lookup"><span data-stu-id="df1b5-107">EXAMPLES</span></span>

### <span data-ttu-id="df1b5-108">範例1：取得 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="df1b5-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="df1b5-109">這個命令會在主機池中取得 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="df1b5-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="df1b5-110">參數</span><span class="sxs-lookup"><span data-stu-id="df1b5-110">PARAMETERS</span></span>

### <span data-ttu-id="df1b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1b5-111">-DefaultProfile</span></span>
<span data-ttu-id="df1b5-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df1b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1b5-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="df1b5-113">-HostPoolName</span></span>
<span data-ttu-id="df1b5-114">主機池名稱</span><span class="sxs-lookup"><span data-stu-id="df1b5-114">Host Pool Name</span></span>

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

### <span data-ttu-id="df1b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="df1b5-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="df1b5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="df1b5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df1b5-117">-SubscriptionId</span></span>
<span data-ttu-id="df1b5-118">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="df1b5-118">Subscription Id</span></span>

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

### <span data-ttu-id="df1b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1b5-119">CommonParameters</span></span>
<span data-ttu-id="df1b5-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df1b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1b5-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df1b5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1b5-122">輸入</span><span class="sxs-lookup"><span data-stu-id="df1b5-122">INPUTS</span></span>

## <span data-ttu-id="df1b5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="df1b5-123">OUTPUTS</span></span>

### <span data-ttu-id="df1b5-124">RegistrationInfo （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="df1b5-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.RegistrationInfo</span></span>

## <span data-ttu-id="df1b5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="df1b5-125">NOTES</span></span>

<span data-ttu-id="df1b5-126">別名</span><span class="sxs-lookup"><span data-stu-id="df1b5-126">ALIASES</span></span>

## <span data-ttu-id="df1b5-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="df1b5-127">RELATED LINKS</span></span>

