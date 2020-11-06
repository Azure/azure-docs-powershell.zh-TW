---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442104"
---
# <span data-ttu-id="9d014-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9d014-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="9d014-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d014-102">SYNOPSIS</span></span>
<span data-ttu-id="9d014-103">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="9d014-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="9d014-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d014-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9d014-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d014-105">DESCRIPTION</span></span>
<span data-ttu-id="9d014-106">Save-AzureRmContext Cmdlet 會儲存目前的驗證資訊，以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="9d014-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="9d014-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d014-107">EXAMPLES</span></span>

### <span data-ttu-id="9d014-108">範例1：儲存目前會話的內容</span><span class="sxs-lookup"><span data-stu-id="9d014-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="9d014-109">這個範例會將目前會話的 Azure 內容儲存至提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="9d014-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="9d014-110">範例2：儲存指定內容</span><span class="sxs-lookup"><span data-stu-id="9d014-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="9d014-111">這個範例會將傳遞到 Cmdlet 的 Azure 內容儲存到提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="9d014-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="9d014-112">參數</span><span class="sxs-lookup"><span data-stu-id="9d014-112">PARAMETERS</span></span>

### <span data-ttu-id="9d014-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9d014-113">-Force</span></span>
<span data-ttu-id="9d014-114">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="9d014-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="9d014-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9d014-115">-Path</span></span>
<span data-ttu-id="9d014-116">指定要儲存驗證資訊之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9d014-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d014-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9d014-117">-Profile</span></span>
<span data-ttu-id="9d014-118">指定此 Cmdlet 讀取的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="9d014-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="9d014-119">如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。</span><span class="sxs-lookup"><span data-stu-id="9d014-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d014-120">-確認</span><span class="sxs-lookup"><span data-stu-id="9d014-120">-Confirm</span></span>
<span data-ttu-id="9d014-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d014-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d014-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d014-122">-WhatIf</span></span>
<span data-ttu-id="9d014-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d014-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d014-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d014-124">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9d014-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9d014-125">INPUTS</span></span>

### <span data-ttu-id="9d014-126">AzureRMProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="9d014-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="9d014-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9d014-127">OUTPUTS</span></span>

### <span data-ttu-id="9d014-128">PSAzureProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d014-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="9d014-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9d014-129">NOTES</span></span>

## <span data-ttu-id="9d014-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d014-130">RELATED LINKS</span></span>

