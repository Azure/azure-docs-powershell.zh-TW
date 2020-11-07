---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 555409187d2d48476a731be344d0404efddc946c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794139"
---
# <span data-ttu-id="b630f-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="b630f-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="b630f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b630f-102">SYNOPSIS</span></span>
<span data-ttu-id="b630f-103">顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="b630f-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="b630f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b630f-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b630f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b630f-105">DESCRIPTION</span></span>
<span data-ttu-id="b630f-106">顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="b630f-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="b630f-107">示例</span><span class="sxs-lookup"><span data-stu-id="b630f-107">EXAMPLES</span></span>

### <span data-ttu-id="b630f-108">取得目前會話的內容儲存中繼資料</span><span class="sxs-lookup"><span data-stu-id="b630f-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="b630f-109">取得有關內容是否已儲存的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b630f-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="b630f-110">在上述範例中，已停用 [自動儲存] 功能。</span><span class="sxs-lookup"><span data-stu-id="b630f-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="b630f-111">取得目前使用者的內容儲存中繼資料</span><span class="sxs-lookup"><span data-stu-id="b630f-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="b630f-112">取得目前使用者預設會儲存內容的相關詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b630f-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="b630f-113">請注意，這可能與目前會話中使用中的設定不同。</span><span class="sxs-lookup"><span data-stu-id="b630f-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="b630f-114">在上述範例中，已啟用 [自動儲存] 功能，並將資料儲存到預設位置。</span><span class="sxs-lookup"><span data-stu-id="b630f-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="b630f-115">參數</span><span class="sxs-lookup"><span data-stu-id="b630f-115">PARAMETERS</span></span>

### <span data-ttu-id="b630f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b630f-116">-DefaultProfile</span></span>
<span data-ttu-id="b630f-117">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="b630f-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b630f-118">-範圍</span><span class="sxs-lookup"><span data-stu-id="b630f-118">-Scope</span></span>
<span data-ttu-id="b630f-119">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="b630f-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b630f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b630f-120">CommonParameters</span></span>
<span data-ttu-id="b630f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b630f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b630f-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b630f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b630f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b630f-123">INPUTS</span></span>

### <span data-ttu-id="b630f-124">所有</span><span class="sxs-lookup"><span data-stu-id="b630f-124">None</span></span>

## <span data-ttu-id="b630f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b630f-125">OUTPUTS</span></span>

### <span data-ttu-id="b630f-126">CoNtextAutosaveSettings 的常見驗證。</span><span class="sxs-lookup"><span data-stu-id="b630f-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b630f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b630f-127">NOTES</span></span>

## <span data-ttu-id="b630f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b630f-128">RELATED LINKS</span></span>
