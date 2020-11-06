---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447290"
---
# <span data-ttu-id="3f2ee-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3f2ee-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="3f2ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2ee-103">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f2ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f2ee-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2ee-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f2ee-105">DESCRIPTION</span></span>
<span data-ttu-id="3f2ee-106">Save-AzureRmContext Cmdlet 會儲存目前的驗證資訊，以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="3f2ee-107">示例</span><span class="sxs-lookup"><span data-stu-id="3f2ee-107">EXAMPLES</span></span>

### <span data-ttu-id="3f2ee-108">範例1：儲存目前會話的內容</span><span class="sxs-lookup"><span data-stu-id="3f2ee-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="3f2ee-109">這個範例會將目前會話的 Azure 內容儲存至提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="3f2ee-110">範例2：儲存指定內容</span><span class="sxs-lookup"><span data-stu-id="3f2ee-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="3f2ee-111">這個範例會將傳遞到 Cmdlet 的 Azure 內容儲存到提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="3f2ee-112">參數</span><span class="sxs-lookup"><span data-stu-id="3f2ee-112">PARAMETERS</span></span>

### <span data-ttu-id="3f2ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2ee-113">-DefaultProfile</span></span>
<span data-ttu-id="3f2ee-114">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f2ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f2ee-115">-Force</span></span>
<span data-ttu-id="3f2ee-116">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="3f2ee-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="3f2ee-117">-Path</span><span class="sxs-lookup"><span data-stu-id="3f2ee-117">-Path</span></span>
<span data-ttu-id="3f2ee-118">指定要儲存驗證資訊之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="3f2ee-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3f2ee-119">-Profile</span></span>
<span data-ttu-id="3f2ee-120">指定此 Cmdlet 讀取的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="3f2ee-121">如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="3f2ee-122">-確認</span><span class="sxs-lookup"><span data-stu-id="3f2ee-122">-Confirm</span></span>
<span data-ttu-id="3f2ee-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f2ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2ee-124">-WhatIf</span></span>
<span data-ttu-id="3f2ee-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f2ee-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f2ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2ee-127">CommonParameters</span></span>
<span data-ttu-id="3f2ee-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2ee-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2ee-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3f2ee-130">INPUTS</span></span>

### <span data-ttu-id="3f2ee-131">AzureRmProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="3f2ee-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>
<span data-ttu-id="3f2ee-132">參數：設定檔 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3f2ee-132">Parameters: Profile (ByValue)</span></span>

## <span data-ttu-id="3f2ee-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3f2ee-133">OUTPUTS</span></span>

### <span data-ttu-id="3f2ee-134">PSAzureProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f2ee-134">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="3f2ee-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3f2ee-135">NOTES</span></span>

## <span data-ttu-id="3f2ee-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f2ee-136">RELATED LINKS</span></span>
