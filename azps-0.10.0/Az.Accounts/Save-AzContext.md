---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 07e565031a5c29ae1be78246cad95326952007e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794117"
---
# <span data-ttu-id="61b30-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="61b30-101">Save-AzContext</span></span>

## <span data-ttu-id="61b30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61b30-102">SYNOPSIS</span></span>
<span data-ttu-id="61b30-103">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="61b30-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="61b30-104">句法</span><span class="sxs-lookup"><span data-stu-id="61b30-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61b30-105">說明</span><span class="sxs-lookup"><span data-stu-id="61b30-105">DESCRIPTION</span></span>
<span data-ttu-id="61b30-106">Save-AzContext Cmdlet 會儲存目前的驗證資訊，以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="61b30-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="61b30-107">示例</span><span class="sxs-lookup"><span data-stu-id="61b30-107">EXAMPLES</span></span>

### <span data-ttu-id="61b30-108">範例1：儲存目前會話的內容</span><span class="sxs-lookup"><span data-stu-id="61b30-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="61b30-109">這個範例會將目前會話的 Azure 內容儲存至提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="61b30-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="61b30-110">範例2：儲存指定內容</span><span class="sxs-lookup"><span data-stu-id="61b30-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="61b30-111">這個範例會將傳遞到 Cmdlet 的 Azure 內容儲存到提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="61b30-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="61b30-112">參數</span><span class="sxs-lookup"><span data-stu-id="61b30-112">PARAMETERS</span></span>

### <span data-ttu-id="61b30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b30-113">-DefaultProfile</span></span>
<span data-ttu-id="61b30-114">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61b30-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61b30-115">-Force</span><span class="sxs-lookup"><span data-stu-id="61b30-115">-Force</span></span>
<span data-ttu-id="61b30-116">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="61b30-116">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b30-117">-Path</span><span class="sxs-lookup"><span data-stu-id="61b30-117">-Path</span></span>
<span data-ttu-id="61b30-118">指定要儲存驗證資訊之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="61b30-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b30-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="61b30-119">-Profile</span></span>
<span data-ttu-id="61b30-120">指定此 Cmdlet 讀取的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="61b30-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="61b30-121">如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。</span><span class="sxs-lookup"><span data-stu-id="61b30-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61b30-122">-確認</span><span class="sxs-lookup"><span data-stu-id="61b30-122">-Confirm</span></span>
<span data-ttu-id="61b30-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61b30-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b30-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61b30-124">-WhatIf</span></span>
<span data-ttu-id="61b30-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61b30-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61b30-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61b30-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b30-127">CommonParameters</span></span>
<span data-ttu-id="61b30-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61b30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b30-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61b30-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b30-130">輸入</span><span class="sxs-lookup"><span data-stu-id="61b30-130">INPUTS</span></span>

### <span data-ttu-id="61b30-131">AzureRmProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="61b30-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="61b30-132">輸出</span><span class="sxs-lookup"><span data-stu-id="61b30-132">OUTPUTS</span></span>

### <span data-ttu-id="61b30-133">PSAzureProfile 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="61b30-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="61b30-134">筆記</span><span class="sxs-lookup"><span data-stu-id="61b30-134">NOTES</span></span>

## <span data-ttu-id="61b30-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="61b30-135">RELATED LINKS</span></span>