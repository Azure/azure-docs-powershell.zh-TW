---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: aa1bfb0760480d5c2e24e113653037ecb83a9f6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917526"
---
# <span data-ttu-id="5a870-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="5a870-101">Get-AzDefault</span></span>

## <span data-ttu-id="5a870-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a870-102">SYNOPSIS</span></span>
<span data-ttu-id="5a870-103">取得使用者目前上下文所設定的預設設定。</span><span class="sxs-lookup"><span data-stu-id="5a870-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="5a870-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a870-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a870-105">描述</span><span class="sxs-lookup"><span data-stu-id="5a870-105">DESCRIPTION</span></span>
<span data-ttu-id="5a870-106">此Get-AzDefault Cmdlet 會獲得使用者目前內容中設為預設值的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5a870-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="5a870-107">例子</span><span class="sxs-lookup"><span data-stu-id="5a870-107">EXAMPLES</span></span>

### <span data-ttu-id="5a870-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a870-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="5a870-109">如果已設定預設值，此命令會返回目前的預設值，如果沒有設定預設值，則不會返回任何值。</span><span class="sxs-lookup"><span data-stu-id="5a870-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="5a870-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="5a870-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="5a870-111">如果有預設設定，此命令會返回目前的預設資源群組，如果沒有設定預設值，則不會返回任何專案。</span><span class="sxs-lookup"><span data-stu-id="5a870-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="5a870-112">參數</span><span class="sxs-lookup"><span data-stu-id="5a870-112">PARAMETERS</span></span>

### <span data-ttu-id="5a870-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a870-113">-DefaultProfile</span></span>
<span data-ttu-id="5a870-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a870-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a870-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a870-115">-ResourceGroup</span></span>
<span data-ttu-id="5a870-116">顯示預設資源群組</span><span class="sxs-lookup"><span data-stu-id="5a870-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="5a870-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a870-117">CommonParameters</span></span>
<span data-ttu-id="5a870-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a870-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a870-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a870-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a870-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5a870-120">INPUTS</span></span>

### <span data-ttu-id="5a870-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a870-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a870-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5a870-122">OUTPUTS</span></span>

### <span data-ttu-id="5a870-123">Microsoft.Azure.Commands.Profile.models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a870-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="5a870-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5a870-124">NOTES</span></span>

## <span data-ttu-id="5a870-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a870-125">RELATED LINKS</span></span>
