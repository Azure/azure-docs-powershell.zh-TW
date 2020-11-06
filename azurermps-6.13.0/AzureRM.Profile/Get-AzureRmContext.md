---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: dbe93ca98fe8cf7a0a22f2b52a17a17e7222c261
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446923"
---
# <span data-ttu-id="54c87-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="54c87-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="54c87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54c87-102">SYNOPSIS</span></span>
<span data-ttu-id="54c87-103">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="54c87-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54c87-104">句法</span><span class="sxs-lookup"><span data-stu-id="54c87-104">SYNTAX</span></span>

### <span data-ttu-id="54c87-105">GetSingleCoNtext (預設) </span><span class="sxs-lookup"><span data-stu-id="54c87-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="54c87-106">ListAllCoNtexts</span><span class="sxs-lookup"><span data-stu-id="54c87-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c87-107">說明</span><span class="sxs-lookup"><span data-stu-id="54c87-107">DESCRIPTION</span></span>
<span data-ttu-id="54c87-108">Get-AzureRmContext Cmdlet 會取得目前用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="54c87-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="54c87-109">這個 Cmdlet 會取得 Active Directory 帳戶、Active Directory 租使用者、Azure 訂閱及目標 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="54c87-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="54c87-110">Azure 資源管理器 Cmdlet 會在進行 Azure 資源管理員要求時預設使用這些設定。</span><span class="sxs-lookup"><span data-stu-id="54c87-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="54c87-111">示例</span><span class="sxs-lookup"><span data-stu-id="54c87-111">EXAMPLES</span></span>

### <span data-ttu-id="54c87-112">範例1：取得目前的內容</span><span class="sxs-lookup"><span data-stu-id="54c87-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="54c87-113">在這個範例中，我們會使用 Connect AzureRmAccount，透過 Azure 訂閱登入我們的帳戶，然後我們會呼叫 AzureRmCoNtext 以取得目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="54c87-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="54c87-114">範例2：列出所有可用的內容</span><span class="sxs-lookup"><span data-stu-id="54c87-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="54c87-115">在這個範例中，會顯示所有目前可用的上下文。</span><span class="sxs-lookup"><span data-stu-id="54c87-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="54c87-116">使用者可以使用 AzureRmCoNtext 選取其中一個上下文。</span><span class="sxs-lookup"><span data-stu-id="54c87-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="54c87-117">參數</span><span class="sxs-lookup"><span data-stu-id="54c87-117">PARAMETERS</span></span>

### <span data-ttu-id="54c87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c87-118">-DefaultProfile</span></span>
<span data-ttu-id="54c87-119">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="54c87-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c87-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="54c87-120">-ListAvailable</span></span>
<span data-ttu-id="54c87-121">列出目前會話中所有可用的上下文。</span><span class="sxs-lookup"><span data-stu-id="54c87-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="54c87-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="54c87-122">-Name</span></span>
<span data-ttu-id="54c87-123">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="54c87-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c87-124">CommonParameters</span></span>
<span data-ttu-id="54c87-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54c87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c87-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54c87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c87-127">輸入</span><span class="sxs-lookup"><span data-stu-id="54c87-127">INPUTS</span></span>

### <span data-ttu-id="54c87-128">所有</span><span class="sxs-lookup"><span data-stu-id="54c87-128">None</span></span>

## <span data-ttu-id="54c87-129">輸出</span><span class="sxs-lookup"><span data-stu-id="54c87-129">OUTPUTS</span></span>

### <span data-ttu-id="54c87-130">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="54c87-130">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="54c87-131">筆記</span><span class="sxs-lookup"><span data-stu-id="54c87-131">NOTES</span></span>

## <span data-ttu-id="54c87-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="54c87-132">RELATED LINKS</span></span>

[<span data-ttu-id="54c87-133">Set-AzureRMCoNtext</span><span class="sxs-lookup"><span data-stu-id="54c87-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

