---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284761"
---
# <span data-ttu-id="665bc-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="665bc-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="665bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="665bc-102">SYNOPSIS</span></span>
<span data-ttu-id="665bc-103">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="665bc-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="665bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="665bc-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="665bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="665bc-105">DESCRIPTION</span></span>
<span data-ttu-id="665bc-106">取得 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="665bc-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="665bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="665bc-107">EXAMPLES</span></span>

### <span data-ttu-id="665bc-108">範例1：取得 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="665bc-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="665bc-109">這個命令會在主機池中取得 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="665bc-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="665bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="665bc-110">PARAMETERS</span></span>

### <span data-ttu-id="665bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="665bc-111">-DefaultProfile</span></span>
<span data-ttu-id="665bc-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="665bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="665bc-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="665bc-113">-HostPoolName</span></span>
<span data-ttu-id="665bc-114">主機池名稱</span><span class="sxs-lookup"><span data-stu-id="665bc-114">Host Pool Name</span></span>

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

### <span data-ttu-id="665bc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="665bc-115">-ResourceGroupName</span></span>
<span data-ttu-id="665bc-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="665bc-116">Resource Group Name</span></span>

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

### <span data-ttu-id="665bc-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="665bc-117">-SubscriptionId</span></span>
<span data-ttu-id="665bc-118">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="665bc-118">Subscription Id</span></span>

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

### <span data-ttu-id="665bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="665bc-119">CommonParameters</span></span>
<span data-ttu-id="665bc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="665bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="665bc-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="665bc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="665bc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="665bc-122">INPUTS</span></span>

## <span data-ttu-id="665bc-123">輸出</span><span class="sxs-lookup"><span data-stu-id="665bc-123">OUTPUTS</span></span>

### <span data-ttu-id="665bc-124">RegistrationInfo （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="665bc-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="665bc-125">筆記</span><span class="sxs-lookup"><span data-stu-id="665bc-125">NOTES</span></span>

<span data-ttu-id="665bc-126">別名</span><span class="sxs-lookup"><span data-stu-id="665bc-126">ALIASES</span></span>

## <span data-ttu-id="665bc-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="665bc-127">RELATED LINKS</span></span>

