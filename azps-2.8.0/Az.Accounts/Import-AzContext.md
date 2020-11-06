---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 145c5f65b00da7f143b04d526b8bcd959d323d12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614188"
---
# <span data-ttu-id="eceaf-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="eceaf-101">Import-AzContext</span></span>

## <span data-ttu-id="eceaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eceaf-102">SYNOPSIS</span></span>
<span data-ttu-id="eceaf-103">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="eceaf-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="eceaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="eceaf-104">SYNTAX</span></span>

### <span data-ttu-id="eceaf-105">ProfileFromDisk (預設) </span><span class="sxs-lookup"><span data-stu-id="eceaf-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eceaf-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="eceaf-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eceaf-107">說明</span><span class="sxs-lookup"><span data-stu-id="eceaf-107">DESCRIPTION</span></span>
<span data-ttu-id="eceaf-108">Import-AzContext Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。</span><span class="sxs-lookup"><span data-stu-id="eceaf-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="eceaf-109">您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="eceaf-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="eceaf-110">示例</span><span class="sxs-lookup"><span data-stu-id="eceaf-110">EXAMPLES</span></span>

### <span data-ttu-id="eceaf-111">範例1：從 AzureRmProfile 匯入內容</span><span class="sxs-lookup"><span data-stu-id="eceaf-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="eceaf-112">這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 匯入內容。</span><span class="sxs-lookup"><span data-stu-id="eceaf-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="eceaf-113">範例2：從 JSON 檔案匯入內容</span><span class="sxs-lookup"><span data-stu-id="eceaf-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="eceaf-114">這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取內容。</span><span class="sxs-lookup"><span data-stu-id="eceaf-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="eceaf-115">您可以從 [儲存-AzCoNtext] 建立此 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="eceaf-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="eceaf-116">參數</span><span class="sxs-lookup"><span data-stu-id="eceaf-116">PARAMETERS</span></span>

### <span data-ttu-id="eceaf-117">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="eceaf-117">-AzureContext</span></span>
<span data-ttu-id="eceaf-118">{{Fill AzureCoNtext 說明}}</span><span class="sxs-lookup"><span data-stu-id="eceaf-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="eceaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eceaf-119">-DefaultProfile</span></span>
<span data-ttu-id="eceaf-120">用於與 azure 進行通訊的認證、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eceaf-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eceaf-121">-Path</span><span class="sxs-lookup"><span data-stu-id="eceaf-121">-Path</span></span>
<span data-ttu-id="eceaf-122">指定使用 Save AzCoNtext 儲存之內容資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="eceaf-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="eceaf-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="eceaf-123">-Scope</span></span>
<span data-ttu-id="eceaf-124">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="eceaf-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="eceaf-125">-確認</span><span class="sxs-lookup"><span data-stu-id="eceaf-125">-Confirm</span></span>
<span data-ttu-id="eceaf-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eceaf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eceaf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eceaf-127">-WhatIf</span></span>
<span data-ttu-id="eceaf-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eceaf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eceaf-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eceaf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eceaf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eceaf-130">CommonParameters</span></span>
<span data-ttu-id="eceaf-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eceaf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eceaf-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eceaf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eceaf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="eceaf-133">INPUTS</span></span>

### <span data-ttu-id="eceaf-134">AzureRmProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="eceaf-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="eceaf-135">System.object</span><span class="sxs-lookup"><span data-stu-id="eceaf-135">System.String</span></span>

## <span data-ttu-id="eceaf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="eceaf-136">OUTPUTS</span></span>

### <span data-ttu-id="eceaf-137">PSAzureProfile 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="eceaf-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="eceaf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="eceaf-138">NOTES</span></span>

## <span data-ttu-id="eceaf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="eceaf-139">RELATED LINKS</span></span>
