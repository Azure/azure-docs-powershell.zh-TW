---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: f73ca19ffa2c68599a5244d41b39d90ebbd2835a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907837"
---
# <span data-ttu-id="b6178-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="b6178-101">Save-AzContext</span></span>

## <span data-ttu-id="b6178-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6178-102">SYNOPSIS</span></span>
<span data-ttu-id="b6178-103">會保存目前的驗證資訊，以用於其他 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="b6178-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="b6178-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6178-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6178-105">描述</span><span class="sxs-lookup"><span data-stu-id="b6178-105">DESCRIPTION</span></span>
<span data-ttu-id="b6178-106">Cmdlet Save-AzContext目前的驗證資訊，以用於其他 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="b6178-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="b6178-107">例子</span><span class="sxs-lookup"><span data-stu-id="b6178-107">EXAMPLES</span></span>

### <span data-ttu-id="b6178-108">範例 1：保存目前會話的上下文</span><span class="sxs-lookup"><span data-stu-id="b6178-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="b6178-109">此範例會將目前會話的 Azure 內容存到提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b6178-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="b6178-110">範例 2：另存一個上下文</span><span class="sxs-lookup"><span data-stu-id="b6178-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="b6178-111">此範例會將傳遞至 Cmdlet 的 Azure 上下文，另存到提供的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b6178-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="b6178-112">參數</span><span class="sxs-lookup"><span data-stu-id="b6178-112">PARAMETERS</span></span>

### <span data-ttu-id="b6178-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6178-113">-DefaultProfile</span></span>
<span data-ttu-id="b6178-114">用於與 azure 通訊的認證、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6178-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6178-115">-強制</span><span class="sxs-lookup"><span data-stu-id="b6178-115">-Force</span></span>
<span data-ttu-id="b6178-116">覆寫已存在的檔案</span><span class="sxs-lookup"><span data-stu-id="b6178-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="b6178-117">-路徑</span><span class="sxs-lookup"><span data-stu-id="b6178-117">-Path</span></span>
<span data-ttu-id="b6178-118">指定要儲存驗證資訊的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b6178-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="b6178-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b6178-119">-Profile</span></span>
<span data-ttu-id="b6178-120">指定此 Cmdlet 讀取的 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="b6178-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="b6178-121">如果您未指定上下文，此 Cmdlet 會從本地預設內容讀取。</span><span class="sxs-lookup"><span data-stu-id="b6178-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="b6178-122">-確認</span><span class="sxs-lookup"><span data-stu-id="b6178-122">-Confirm</span></span>
<span data-ttu-id="b6178-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b6178-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6178-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6178-124">-WhatIf</span></span>
<span data-ttu-id="b6178-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6178-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6178-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6178-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6178-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6178-127">CommonParameters</span></span>
<span data-ttu-id="b6178-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6178-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6178-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6178-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6178-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b6178-130">INPUTS</span></span>

### <span data-ttu-id="b6178-131">Microsoft.Azure.Commands.Common.Authentication.models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="b6178-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="b6178-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b6178-132">OUTPUTS</span></span>

### <span data-ttu-id="b6178-133">Microsoft.Azure.Commands.Profile.models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="b6178-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="b6178-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b6178-134">NOTES</span></span>

## <span data-ttu-id="b6178-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6178-135">RELATED LINKS</span></span>
