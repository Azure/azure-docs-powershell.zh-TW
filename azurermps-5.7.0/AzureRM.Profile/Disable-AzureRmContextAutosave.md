---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444455"
---
# <span data-ttu-id="5408f-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5408f-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="5408f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5408f-102">SYNOPSIS</span></span>
<span data-ttu-id="5408f-103">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="5408f-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="5408f-104">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="5408f-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5408f-105">句法</span><span class="sxs-lookup"><span data-stu-id="5408f-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5408f-106">說明</span><span class="sxs-lookup"><span data-stu-id="5408f-106">DESCRIPTION</span></span>
<span data-ttu-id="5408f-107">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="5408f-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="5408f-108">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="5408f-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="5408f-109">示例</span><span class="sxs-lookup"><span data-stu-id="5408f-109">EXAMPLES</span></span>

### <span data-ttu-id="5408f-110">停用 autosaving 內容</span><span class="sxs-lookup"><span data-stu-id="5408f-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="5408f-111">停用目前使用者的自動儲存功能。</span><span class="sxs-lookup"><span data-stu-id="5408f-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="5408f-112">參數</span><span class="sxs-lookup"><span data-stu-id="5408f-112">PARAMETERS</span></span>

### <span data-ttu-id="5408f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5408f-113">-DefaultProfile</span></span>
<span data-ttu-id="5408f-114">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="5408f-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5408f-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="5408f-115">-Scope</span></span>
<span data-ttu-id="5408f-116">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="5408f-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="5408f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="5408f-117">-Confirm</span></span>
<span data-ttu-id="5408f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5408f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5408f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5408f-119">-WhatIf</span></span>
<span data-ttu-id="5408f-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5408f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5408f-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5408f-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5408f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5408f-122">CommonParameters</span></span>
<span data-ttu-id="5408f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5408f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5408f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5408f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5408f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5408f-125">INPUTS</span></span>

### <span data-ttu-id="5408f-126">所有</span><span class="sxs-lookup"><span data-stu-id="5408f-126">None</span></span>

## <span data-ttu-id="5408f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5408f-127">OUTPUTS</span></span>

### <span data-ttu-id="5408f-128">CoNtextAutosaveSettings 的常見驗證。</span><span class="sxs-lookup"><span data-stu-id="5408f-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="5408f-129">目前使用者的 [自動儲存] 設定的相關資訊，包括是否已針對目前使用者啟用自動儲存，以及內容和認證檔案的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="5408f-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="5408f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5408f-130">NOTES</span></span>

## <span data-ttu-id="5408f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5408f-131">RELATED LINKS</span></span>

