---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958204"
---
# <span data-ttu-id="004b5-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="004b5-101">Import-AzContext</span></span>

## <span data-ttu-id="004b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="004b5-102">SYNOPSIS</span></span>
<span data-ttu-id="004b5-103">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="004b5-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="004b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="004b5-104">SYNTAX</span></span>

### <span data-ttu-id="004b5-105">ProfileFromDisk (預設) </span><span class="sxs-lookup"><span data-stu-id="004b5-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b5-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="004b5-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="004b5-107">說明</span><span class="sxs-lookup"><span data-stu-id="004b5-107">DESCRIPTION</span></span>
<span data-ttu-id="004b5-108">Import-AzContext Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。</span><span class="sxs-lookup"><span data-stu-id="004b5-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="004b5-109">您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="004b5-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="004b5-110">示例</span><span class="sxs-lookup"><span data-stu-id="004b5-110">EXAMPLES</span></span>

### <span data-ttu-id="004b5-111">範例1：從 AzureRmProfile 匯入內容</span><span class="sxs-lookup"><span data-stu-id="004b5-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="004b5-112">這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 匯入內容。</span><span class="sxs-lookup"><span data-stu-id="004b5-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="004b5-113">範例2：從 JSON 檔案匯入內容</span><span class="sxs-lookup"><span data-stu-id="004b5-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="004b5-114">這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取內容。</span><span class="sxs-lookup"><span data-stu-id="004b5-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="004b5-115">您可以從 [儲存-AzCoNtext] 建立此 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="004b5-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="004b5-116">參數</span><span class="sxs-lookup"><span data-stu-id="004b5-116">PARAMETERS</span></span>

### <span data-ttu-id="004b5-117">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="004b5-117">-AzureContext</span></span>
<span data-ttu-id="004b5-118">{{Fill AzureCoNtext 說明}}</span><span class="sxs-lookup"><span data-stu-id="004b5-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="004b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004b5-119">-DefaultProfile</span></span>
<span data-ttu-id="004b5-120">用於與 azure 進行通訊的認證、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="004b5-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="004b5-121">-Path</span><span class="sxs-lookup"><span data-stu-id="004b5-121">-Path</span></span>
<span data-ttu-id="004b5-122">指定使用 Save AzCoNtext 儲存之內容資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="004b5-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="004b5-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="004b5-123">-Scope</span></span>
<span data-ttu-id="004b5-124">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="004b5-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="004b5-125">-確認</span><span class="sxs-lookup"><span data-stu-id="004b5-125">-Confirm</span></span>
<span data-ttu-id="004b5-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="004b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004b5-127">-WhatIf</span></span>
<span data-ttu-id="004b5-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="004b5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="004b5-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="004b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004b5-130">CommonParameters</span></span>
<span data-ttu-id="004b5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="004b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004b5-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="004b5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004b5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="004b5-133">INPUTS</span></span>

### <span data-ttu-id="004b5-134">AzureRmProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="004b5-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="004b5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="004b5-135">System.String</span></span>

## <span data-ttu-id="004b5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="004b5-136">OUTPUTS</span></span>

### <span data-ttu-id="004b5-137">PSAzureProfile 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="004b5-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="004b5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="004b5-138">NOTES</span></span>

## <span data-ttu-id="004b5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="004b5-139">RELATED LINKS</span></span>
