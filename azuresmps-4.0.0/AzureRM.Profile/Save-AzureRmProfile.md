---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442972"
---
# <span data-ttu-id="f54bb-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="f54bb-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="f54bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f54bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f54bb-103">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="f54bb-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f54bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="f54bb-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f54bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="f54bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f54bb-106">Save-AzureRmProfile Cmdlet 會儲存目前的驗證資訊，以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="f54bb-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f54bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="f54bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f54bb-108">範例1：儲存目前會話的設定檔</span><span class="sxs-lookup"><span data-stu-id="f54bb-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="f54bb-109">這個範例會將目前會話的 Azure 設定檔儲存至提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="f54bb-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="f54bb-110">範例2：儲存指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="f54bb-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="f54bb-111">這個範例會將傳遞到 Cmdlet 的 Azure 設定檔儲存到提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="f54bb-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="f54bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="f54bb-112">PARAMETERS</span></span>

### <span data-ttu-id="f54bb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f54bb-113">-Force</span></span>
<span data-ttu-id="f54bb-114">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="f54bb-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54bb-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f54bb-115">-Path</span></span>
<span data-ttu-id="f54bb-116">指定要儲存驗證資訊之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f54bb-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54bb-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f54bb-117">-Profile</span></span>
<span data-ttu-id="f54bb-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f54bb-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f54bb-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f54bb-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f54bb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f54bb-120">-Confirm</span></span>
<span data-ttu-id="f54bb-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f54bb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f54bb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f54bb-122">-WhatIf</span></span>
<span data-ttu-id="f54bb-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f54bb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f54bb-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f54bb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f54bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54bb-125">CommonParameters</span></span>
<span data-ttu-id="f54bb-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f54bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54bb-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f54bb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54bb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f54bb-128">INPUTS</span></span>

## <span data-ttu-id="f54bb-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f54bb-129">OUTPUTS</span></span>

### <span data-ttu-id="f54bb-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f54bb-130">PSAzureProfile</span></span>

## <span data-ttu-id="f54bb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f54bb-131">NOTES</span></span>

## <span data-ttu-id="f54bb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f54bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="f54bb-133">選取-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="f54bb-133">Select-AzureRMProfile</span></span>]()

