---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: e56452d14f9c0f17b4f744d08fdd5911fb39aff5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794141"
---
# <span data-ttu-id="affdc-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="affdc-101">Get-AzContext</span></span>

## <span data-ttu-id="affdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="affdc-102">SYNOPSIS</span></span>
<span data-ttu-id="affdc-103">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="affdc-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="affdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="affdc-104">SYNTAX</span></span>

### <span data-ttu-id="affdc-105">GetSingleCoNtext (預設) </span><span class="sxs-lookup"><span data-stu-id="affdc-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="affdc-106">ListAllCoNtexts</span><span class="sxs-lookup"><span data-stu-id="affdc-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="affdc-107">說明</span><span class="sxs-lookup"><span data-stu-id="affdc-107">DESCRIPTION</span></span>
<span data-ttu-id="affdc-108">Get-AzContext Cmdlet 會取得目前用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="affdc-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="affdc-109">這個 Cmdlet 會取得 Active Directory 帳戶、Active Directory 租使用者、Azure 訂閱及目標 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="affdc-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="affdc-110">Azure 資源管理器 Cmdlet 會在進行 Azure 資源管理員要求時預設使用這些設定。</span><span class="sxs-lookup"><span data-stu-id="affdc-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="affdc-111">示例</span><span class="sxs-lookup"><span data-stu-id="affdc-111">EXAMPLES</span></span>

### <span data-ttu-id="affdc-112">範例1：取得目前的內容</span><span class="sxs-lookup"><span data-stu-id="affdc-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="affdc-113">在這個範例中，我們會使用 Connect AzAccount，透過 Azure 訂閱登入我們的帳戶，然後我們會呼叫 AzCoNtext 以取得目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="affdc-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="affdc-114">範例2：列出所有可用的內容</span><span class="sxs-lookup"><span data-stu-id="affdc-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="affdc-115">在這個範例中，會顯示所有目前可用的上下文。</span><span class="sxs-lookup"><span data-stu-id="affdc-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="affdc-116">使用者可以使用 AzCoNtext 選取其中一個上下文。</span><span class="sxs-lookup"><span data-stu-id="affdc-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="affdc-117">參數</span><span class="sxs-lookup"><span data-stu-id="affdc-117">PARAMETERS</span></span>

### <span data-ttu-id="affdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affdc-118">-DefaultProfile</span></span>
<span data-ttu-id="affdc-119">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="affdc-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="affdc-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="affdc-120">-ListAvailable</span></span>
<span data-ttu-id="affdc-121">列出目前會話中所有可用的上下文。</span><span class="sxs-lookup"><span data-stu-id="affdc-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="affdc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="affdc-122">-Name</span></span>
<span data-ttu-id="affdc-123">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="affdc-123">The name of the context</span></span>

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

### <span data-ttu-id="affdc-124">-RefreshCoNtextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="affdc-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="affdc-125">從權杖緩存重新整理內容</span><span class="sxs-lookup"><span data-stu-id="affdc-125">Refresh contexts from token cache</span></span>

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

### <span data-ttu-id="affdc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affdc-126">CommonParameters</span></span>
<span data-ttu-id="affdc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="affdc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affdc-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="affdc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affdc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="affdc-129">INPUTS</span></span>

### <span data-ttu-id="affdc-130">所有</span><span class="sxs-lookup"><span data-stu-id="affdc-130">None</span></span>

## <span data-ttu-id="affdc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="affdc-131">OUTPUTS</span></span>

### <span data-ttu-id="affdc-132">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="affdc-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="affdc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="affdc-133">NOTES</span></span>

## <span data-ttu-id="affdc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="affdc-134">RELATED LINKS</span></span>

[<span data-ttu-id="affdc-135">Set-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="affdc-135">Set-AzContext</span></span>](./Set-AzContext.md)

