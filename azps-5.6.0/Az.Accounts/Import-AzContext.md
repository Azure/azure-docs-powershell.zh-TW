---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 18dd703551603ed03eb36d19af04fcd3ab6938f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902678"
---
# <span data-ttu-id="53962-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="53962-101">Import-AzContext</span></span>

## <span data-ttu-id="53962-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53962-102">SYNOPSIS</span></span>
<span data-ttu-id="53962-103">載入檔案中的 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="53962-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="53962-104">語法</span><span class="sxs-lookup"><span data-stu-id="53962-104">SYNTAX</span></span>

### <span data-ttu-id="53962-105">ProfileFrom在 (中) </span><span class="sxs-lookup"><span data-stu-id="53962-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53962-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="53962-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53962-107">描述</span><span class="sxs-lookup"><span data-stu-id="53962-107">DESCRIPTION</span></span>
<span data-ttu-id="53962-108">Cmdlet Import-AzContext載入來自檔案的驗證資訊，以設定 Azure 環境和上下文。</span><span class="sxs-lookup"><span data-stu-id="53962-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="53962-109">您目前會話執行 Cmdlet 會使用此資訊向 Azure Resource Manager 驗證要求。</span><span class="sxs-lookup"><span data-stu-id="53962-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="53962-110">例子</span><span class="sxs-lookup"><span data-stu-id="53962-110">EXAMPLES</span></span>

### <span data-ttu-id="53962-111">範例 1：從 AzureRmProfile 中輸入內容</span><span class="sxs-lookup"><span data-stu-id="53962-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="53962-112">此範例會從傳遞至 Cmdlet 的 PSAzureProfile 中，將內容導入。</span><span class="sxs-lookup"><span data-stu-id="53962-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="53962-113">範例 2：從 JSON 檔案中輸入內容</span><span class="sxs-lookup"><span data-stu-id="53962-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="53962-114">此範例會從 JSON 檔案選取傳遞至 Cmdlet 的內容。</span><span class="sxs-lookup"><span data-stu-id="53962-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="53962-115">此 JSON 檔案可以從 Save-AzCoNtext 建立。</span><span class="sxs-lookup"><span data-stu-id="53962-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="53962-116">參數</span><span class="sxs-lookup"><span data-stu-id="53962-116">PARAMETERS</span></span>

### <span data-ttu-id="53962-117">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="53962-117">-AzureContext</span></span>
<span data-ttu-id="53962-118">{{Fill AzureCoNtext Description}}</span><span class="sxs-lookup"><span data-stu-id="53962-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="53962-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53962-119">-DefaultProfile</span></span>
<span data-ttu-id="53962-120">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="53962-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53962-121">-路徑</span><span class="sxs-lookup"><span data-stu-id="53962-121">-Path</span></span>
<span data-ttu-id="53962-122">指定使用 Save-AzCoNtext 儲存內容資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="53962-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="53962-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="53962-123">-Scope</span></span>
<span data-ttu-id="53962-124">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="53962-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="53962-125">-確認</span><span class="sxs-lookup"><span data-stu-id="53962-125">-Confirm</span></span>
<span data-ttu-id="53962-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="53962-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53962-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53962-127">-WhatIf</span></span>
<span data-ttu-id="53962-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53962-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53962-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53962-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53962-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53962-130">CommonParameters</span></span>
<span data-ttu-id="53962-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53962-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53962-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53962-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53962-133">輸入</span><span class="sxs-lookup"><span data-stu-id="53962-133">INPUTS</span></span>

### <span data-ttu-id="53962-134">Microsoft.Azure.Commands.Common.Authentication.models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="53962-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="53962-135">System.String</span><span class="sxs-lookup"><span data-stu-id="53962-135">System.String</span></span>

## <span data-ttu-id="53962-136">輸出</span><span class="sxs-lookup"><span data-stu-id="53962-136">OUTPUTS</span></span>

### <span data-ttu-id="53962-137">Microsoft.Azure.Commands.Profile.models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="53962-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="53962-138">筆記</span><span class="sxs-lookup"><span data-stu-id="53962-138">NOTES</span></span>

## <span data-ttu-id="53962-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="53962-139">RELATED LINKS</span></span>
