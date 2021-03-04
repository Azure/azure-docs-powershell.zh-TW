---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 2060a1cbe9f002a20b94e82ac9547c5fc96c0e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916692"
---
# <span data-ttu-id="d8533-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="d8533-101">Get-AzContext</span></span>

## <span data-ttu-id="d8533-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8533-102">SYNOPSIS</span></span>
<span data-ttu-id="d8533-103">獲得用來驗證 Azure Resource Manager 要求之中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d8533-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="d8533-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8533-104">SYNTAX</span></span>

### <span data-ttu-id="d8533-105">GetSingleCoNtext (預設) </span><span class="sxs-lookup"><span data-stu-id="d8533-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8533-106">ListAllCoNtexts</span><span class="sxs-lookup"><span data-stu-id="d8533-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8533-107">描述</span><span class="sxs-lookup"><span data-stu-id="d8533-107">DESCRIPTION</span></span>
<span data-ttu-id="d8533-108">Cmdlet Get-AzContext用來驗證 Azure Resource Manager 要求目前的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d8533-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="d8533-109">此 Cmdlet 會獲得 Active Directory 帳戶、Active Directory 租使用者、Azure 訂閱，以及目標 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="d8533-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="d8533-110">根據預設，Azure Resource Manager Cmdlet 在提出 Azure Resource Manager 要求時，會使用這些設定。</span><span class="sxs-lookup"><span data-stu-id="d8533-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="d8533-111">例子</span><span class="sxs-lookup"><span data-stu-id="d8533-111">EXAMPLES</span></span>

### <span data-ttu-id="d8533-112">範例 1：取得目前內容</span><span class="sxs-lookup"><span data-stu-id="d8533-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="d8533-113">在此範例中，我們會使用 Connect-AzAccount 使用 Azure 訂閱登入我們的帳戶，然後撥打 Get-AzCoNtext 以取得目前會話內容。</span><span class="sxs-lookup"><span data-stu-id="d8533-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="d8533-114">範例 2：列出所有可用的上下文</span><span class="sxs-lookup"><span data-stu-id="d8533-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="d8533-115">在此範例中，會顯示所有目前可用的上下文。</span><span class="sxs-lookup"><span data-stu-id="d8533-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="d8533-116">使用者可以使用 Select-AzCoNtext 選取其中一個上下文。</span><span class="sxs-lookup"><span data-stu-id="d8533-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="d8533-117">參數</span><span class="sxs-lookup"><span data-stu-id="d8533-117">PARAMETERS</span></span>

### <span data-ttu-id="d8533-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8533-118">-DefaultProfile</span></span>
<span data-ttu-id="d8533-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d8533-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8533-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="d8533-120">-ListAvailable</span></span>
<span data-ttu-id="d8533-121">列出目前會話內所有可用的上下文。</span><span class="sxs-lookup"><span data-stu-id="d8533-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8533-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8533-122">-Name</span></span>
<span data-ttu-id="d8533-123">內容名稱</span><span class="sxs-lookup"><span data-stu-id="d8533-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8533-124">-RefreshCoNtextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="d8533-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="d8533-125">從權杖緩存重新組織內容</span><span class="sxs-lookup"><span data-stu-id="d8533-125">Refresh contexts from token cache</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8533-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8533-126">CommonParameters</span></span>
<span data-ttu-id="d8533-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8533-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8533-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8533-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8533-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d8533-129">INPUTS</span></span>

### <span data-ttu-id="d8533-130">沒有</span><span class="sxs-lookup"><span data-stu-id="d8533-130">None</span></span>

## <span data-ttu-id="d8533-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d8533-131">OUTPUTS</span></span>

### <span data-ttu-id="d8533-132">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="d8533-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d8533-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d8533-133">NOTES</span></span>

## <span data-ttu-id="d8533-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8533-134">RELATED LINKS</span></span>

[<span data-ttu-id="d8533-135">Set-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="d8533-135">Set-AzContext</span></span>](./Set-AzContext.md)

