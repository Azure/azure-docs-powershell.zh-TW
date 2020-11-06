---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: d785cd364cd67a9d79f8710ef664048b8f54b8ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449567"
---
# <span data-ttu-id="10bda-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="10bda-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="10bda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10bda-102">SYNOPSIS</span></span>
<span data-ttu-id="10bda-103">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="10bda-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10bda-104">句法</span><span class="sxs-lookup"><span data-stu-id="10bda-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10bda-105">說明</span><span class="sxs-lookup"><span data-stu-id="10bda-105">DESCRIPTION</span></span>
<span data-ttu-id="10bda-106">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="10bda-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="10bda-107">示例</span><span class="sxs-lookup"><span data-stu-id="10bda-107">EXAMPLES</span></span>

### <span data-ttu-id="10bda-108">為目前的使用者啟用 autosaving 認證</span><span class="sxs-lookup"><span data-stu-id="10bda-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="10bda-109">針對目前的使用者開啟認證自動儲存。</span><span class="sxs-lookup"><span data-stu-id="10bda-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="10bda-110">每當開啟 powershell 視窗時，就會記住您目前的內容，而不需要登入。</span><span class="sxs-lookup"><span data-stu-id="10bda-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="10bda-111">參數</span><span class="sxs-lookup"><span data-stu-id="10bda-111">PARAMETERS</span></span>

### <span data-ttu-id="10bda-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bda-112">-DefaultProfile</span></span>
<span data-ttu-id="10bda-113">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="10bda-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10bda-114">-範圍</span><span class="sxs-lookup"><span data-stu-id="10bda-114">-Scope</span></span>
<span data-ttu-id="10bda-115">決定內容變更的範圍，例如，wheher 變更只適用于 cusrrent 進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="10bda-115">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="10bda-116">-確認</span><span class="sxs-lookup"><span data-stu-id="10bda-116">-Confirm</span></span>
<span data-ttu-id="10bda-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10bda-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10bda-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10bda-118">-WhatIf</span></span>
<span data-ttu-id="10bda-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10bda-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10bda-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10bda-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10bda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bda-121">CommonParameters</span></span>
<span data-ttu-id="10bda-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10bda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bda-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10bda-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bda-124">輸入</span><span class="sxs-lookup"><span data-stu-id="10bda-124">INPUTS</span></span>

### <span data-ttu-id="10bda-125">所有</span><span class="sxs-lookup"><span data-stu-id="10bda-125">None</span></span>

## <span data-ttu-id="10bda-126">輸出</span><span class="sxs-lookup"><span data-stu-id="10bda-126">OUTPUTS</span></span>

### <span data-ttu-id="10bda-127">CoNtextAutosaveSettings 的常見驗證。</span><span class="sxs-lookup"><span data-stu-id="10bda-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="10bda-128">目前使用者的 [自動儲存] 設定的相關資訊，包括是否已針對目前使用者啟用自動儲存，以及內容和認證檔案的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="10bda-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="10bda-129">筆記</span><span class="sxs-lookup"><span data-stu-id="10bda-129">NOTES</span></span>

## <span data-ttu-id="10bda-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="10bda-130">RELATED LINKS</span></span>

