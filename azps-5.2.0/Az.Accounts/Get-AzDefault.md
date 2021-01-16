---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284543"
---
# <span data-ttu-id="aff4c-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="aff4c-101">Get-AzDefault</span></span>

## <span data-ttu-id="aff4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aff4c-102">SYNOPSIS</span></span>
<span data-ttu-id="aff4c-103">取得使用者在目前內容中設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="aff4c-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="aff4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="aff4c-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aff4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="aff4c-105">DESCRIPTION</span></span>
<span data-ttu-id="aff4c-106">Get-AzDefault Cmdlet 會取得使用者在目前內容中設為預設值的資源群組。</span><span class="sxs-lookup"><span data-stu-id="aff4c-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="aff4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="aff4c-107">EXAMPLES</span></span>

### <span data-ttu-id="aff4c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aff4c-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="aff4c-109">如果沒有設定預設值，這個命令會傳回目前的預設值。</span><span class="sxs-lookup"><span data-stu-id="aff4c-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="aff4c-110">範例2</span><span class="sxs-lookup"><span data-stu-id="aff4c-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="aff4c-111">如果沒有設定預設，這個命令會傳回目前的預設資源群組，或傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="aff4c-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="aff4c-112">參數</span><span class="sxs-lookup"><span data-stu-id="aff4c-112">PARAMETERS</span></span>

### <span data-ttu-id="aff4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff4c-113">-DefaultProfile</span></span>
<span data-ttu-id="aff4c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aff4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aff4c-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aff4c-115">-ResourceGroup</span></span>
<span data-ttu-id="aff4c-116">顯示預設資源群組</span><span class="sxs-lookup"><span data-stu-id="aff4c-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff4c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff4c-117">CommonParameters</span></span>
<span data-ttu-id="aff4c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aff4c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff4c-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aff4c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff4c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="aff4c-120">INPUTS</span></span>

### <span data-ttu-id="aff4c-121">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="aff4c-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aff4c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="aff4c-122">OUTPUTS</span></span>

### <span data-ttu-id="aff4c-123">PSResourceGroup 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="aff4c-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="aff4c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="aff4c-124">NOTES</span></span>

## <span data-ttu-id="aff4c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="aff4c-125">RELATED LINKS</span></span>
