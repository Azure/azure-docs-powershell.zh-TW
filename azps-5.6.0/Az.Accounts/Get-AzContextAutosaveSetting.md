---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 629e35c5b700477fc46565b2da0e5dcf6f3c5b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909258"
---
# <span data-ttu-id="f6232-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="f6232-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="f6232-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6232-102">SYNOPSIS</span></span>
<span data-ttu-id="f6232-103">顯示內容自動儲存功能相關中繼資料，包括內容是否會自動儲存，以及可在哪裡找到已儲存的上下文和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="f6232-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="f6232-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6232-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6232-105">描述</span><span class="sxs-lookup"><span data-stu-id="f6232-105">DESCRIPTION</span></span>
<span data-ttu-id="f6232-106">顯示內容自動儲存功能相關中繼資料，包括內容是否會自動儲存，以及可在哪裡找到已儲存的上下文和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="f6232-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="f6232-107">例子</span><span class="sxs-lookup"><span data-stu-id="f6232-107">EXAMPLES</span></span>

### <span data-ttu-id="f6232-108">取得目前會話的上下文儲存中繼資料</span><span class="sxs-lookup"><span data-stu-id="f6232-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="f6232-109">取得內容是否儲存及儲存位置的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f6232-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="f6232-110">在上例中，自動儲存功能已停用。</span><span class="sxs-lookup"><span data-stu-id="f6232-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="f6232-111">取得目前使用者的上下文儲存中繼資料</span><span class="sxs-lookup"><span data-stu-id="f6232-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="f6232-112">取得目前使用者內容預設是否儲存及儲存位置的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f6232-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="f6232-113">請注意，這可能與目前會話使用中的設定不同。</span><span class="sxs-lookup"><span data-stu-id="f6232-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="f6232-114">在上述範例中，已啟用自動儲存功能，且資料會儲存到預設位置。</span><span class="sxs-lookup"><span data-stu-id="f6232-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="f6232-115">參數</span><span class="sxs-lookup"><span data-stu-id="f6232-115">PARAMETERS</span></span>

### <span data-ttu-id="f6232-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6232-116">-DefaultProfile</span></span>
<span data-ttu-id="f6232-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f6232-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6232-118">-範圍</span><span class="sxs-lookup"><span data-stu-id="f6232-118">-Scope</span></span>
<span data-ttu-id="f6232-119">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="f6232-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f6232-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6232-120">CommonParameters</span></span>
<span data-ttu-id="f6232-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6232-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6232-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6232-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6232-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f6232-123">INPUTS</span></span>

### <span data-ttu-id="f6232-124">沒有</span><span class="sxs-lookup"><span data-stu-id="f6232-124">None</span></span>

## <span data-ttu-id="f6232-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f6232-125">OUTPUTS</span></span>

### <span data-ttu-id="f6232-126">Microsoft.Azure.Commands.Common.Authentication.CoNtextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="f6232-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="f6232-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f6232-127">NOTES</span></span>

## <span data-ttu-id="f6232-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6232-128">RELATED LINKS</span></span>
