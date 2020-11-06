---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/import-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: b78095ef55fa647cc11ea3e2d2b1a49089407747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454180"
---
# <span data-ttu-id="1e2be-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="1e2be-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="1e2be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e2be-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2be-103">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="1e2be-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e2be-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e2be-104">SYNTAX</span></span>

### <span data-ttu-id="1e2be-105">ProfileFromDisk (預設) </span><span class="sxs-lookup"><span data-stu-id="1e2be-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2be-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="1e2be-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e2be-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e2be-107">DESCRIPTION</span></span>
<span data-ttu-id="1e2be-108">Import-AzureRmContext Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。</span><span class="sxs-lookup"><span data-stu-id="1e2be-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="1e2be-109">您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="1e2be-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="1e2be-110">示例</span><span class="sxs-lookup"><span data-stu-id="1e2be-110">EXAMPLES</span></span>

### <span data-ttu-id="1e2be-111">範例1：從 AzureRmProfile 匯入內容</span><span class="sxs-lookup"><span data-stu-id="1e2be-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Connect-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="1e2be-112">這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 匯入內容。</span><span class="sxs-lookup"><span data-stu-id="1e2be-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="1e2be-113">範例2：從 JSON 檔案匯入內容</span><span class="sxs-lookup"><span data-stu-id="1e2be-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="1e2be-114">這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取內容。</span><span class="sxs-lookup"><span data-stu-id="1e2be-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="1e2be-115">您可以從 [儲存-AzureRmCoNtext] 建立此 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="1e2be-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="1e2be-116">參數</span><span class="sxs-lookup"><span data-stu-id="1e2be-116">PARAMETERS</span></span>

### <span data-ttu-id="1e2be-117">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="1e2be-117">-AzureContext</span></span>
<span data-ttu-id="1e2be-118">指定此 Cmdlet 讀取的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="1e2be-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="1e2be-119">如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。</span><span class="sxs-lookup"><span data-stu-id="1e2be-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2be-120">-DefaultProfile</span></span>
<span data-ttu-id="1e2be-121">用於與 azure 進行通訊的認證、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e2be-121">The credentials, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e2be-122">-Path</span><span class="sxs-lookup"><span data-stu-id="1e2be-122">-Path</span></span>
<span data-ttu-id="1e2be-123">指定使用 Save AzureRMCoNtext 儲存之內容資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="1e2be-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2be-124">-範圍</span><span class="sxs-lookup"><span data-stu-id="1e2be-124">-Scope</span></span>
<span data-ttu-id="1e2be-125">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="1e2be-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e2be-126">-確認</span><span class="sxs-lookup"><span data-stu-id="1e2be-126">-Confirm</span></span>
<span data-ttu-id="1e2be-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e2be-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e2be-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2be-128">-WhatIf</span></span>
<span data-ttu-id="1e2be-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e2be-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e2be-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e2be-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e2be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2be-131">CommonParameters</span></span>
<span data-ttu-id="1e2be-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e2be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2be-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e2be-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2be-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1e2be-134">INPUTS</span></span>

### <span data-ttu-id="1e2be-135">AzureRMProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="1e2be-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="1e2be-136">包含用來與 Azure 通訊的認證、帳戶及訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="1e2be-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="1e2be-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1e2be-137">OUTPUTS</span></span>

### <span data-ttu-id="1e2be-138">PSAzureProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="1e2be-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="1e2be-139">包含可用來與 Azure 進行通訊的認證、帳戶及訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="1e2be-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="1e2be-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1e2be-140">NOTES</span></span>

## <span data-ttu-id="1e2be-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e2be-141">RELATED LINKS</span></span>

