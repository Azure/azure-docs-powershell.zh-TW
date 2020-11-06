---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449558"
---
# <span data-ttu-id="fa9e3-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="fa9e3-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="fa9e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9e3-103">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa9e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa9e3-104">SYNTAX</span></span>

### <span data-ttu-id="fa9e3-105">ProfileFromDisk (預設) </span><span class="sxs-lookup"><span data-stu-id="fa9e3-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9e3-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="fa9e3-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9e3-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa9e3-107">DESCRIPTION</span></span>
<span data-ttu-id="fa9e3-108">Import-AzureRmContext Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="fa9e3-109">您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="fa9e3-110">示例</span><span class="sxs-lookup"><span data-stu-id="fa9e3-110">EXAMPLES</span></span>

### <span data-ttu-id="fa9e3-111">範例1：從 AzureRmProfile 匯入內容</span><span class="sxs-lookup"><span data-stu-id="fa9e3-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="fa9e3-112">這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 匯入內容。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="fa9e3-113">範例2：從 JSON 檔案匯入內容</span><span class="sxs-lookup"><span data-stu-id="fa9e3-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="fa9e3-114">這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取內容。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="fa9e3-115">您可以從 [儲存-AzureRmCoNtext] 建立此 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="fa9e3-116">參數</span><span class="sxs-lookup"><span data-stu-id="fa9e3-116">PARAMETERS</span></span>

### <span data-ttu-id="fa9e3-117">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="fa9e3-117">-AzureContext</span></span>
<span data-ttu-id="fa9e3-118">指定此 Cmdlet 讀取的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="fa9e3-119">如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9e3-120">-DefaultProfile</span></span>
<span data-ttu-id="fa9e3-121">用於與 azure 進行通訊的認證、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa9e3-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa9e3-122">-Path</span><span class="sxs-lookup"><span data-stu-id="fa9e3-122">-Path</span></span>
<span data-ttu-id="fa9e3-123">指定使用 Save AzureRMCoNtext 儲存之內容資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e3-124">-範圍</span><span class="sxs-lookup"><span data-stu-id="fa9e3-124">-Scope</span></span>
<span data-ttu-id="fa9e3-125">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="fa9e3-126">-Confirm</span></span>
<span data-ttu-id="fa9e3-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9e3-128">-WhatIf</span></span>
<span data-ttu-id="fa9e3-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa9e3-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9e3-131">CommonParameters</span></span>
<span data-ttu-id="fa9e3-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9e3-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9e3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="fa9e3-134">INPUTS</span></span>

### <span data-ttu-id="fa9e3-135">AzureRMProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="fa9e3-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="fa9e3-136">包含用來與 Azure 通訊的認證、帳戶及訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="fa9e3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fa9e3-137">OUTPUTS</span></span>

### <span data-ttu-id="fa9e3-138">PSAzureProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="fa9e3-139">包含可用來與 Azure 進行通訊的認證、帳戶及訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="fa9e3-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="fa9e3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fa9e3-140">NOTES</span></span>

## <span data-ttu-id="fa9e3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa9e3-141">RELATED LINKS</span></span>

