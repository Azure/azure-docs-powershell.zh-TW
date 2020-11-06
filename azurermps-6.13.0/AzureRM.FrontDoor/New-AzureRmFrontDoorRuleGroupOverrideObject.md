---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443827"
---
# <span data-ttu-id="c8f22-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="c8f22-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="c8f22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8f22-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f22-103">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="c8f22-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f22-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8f22-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8f22-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8f22-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f22-106">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="c8f22-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c8f22-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8f22-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f22-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c8f22-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="c8f22-109">建立 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="c8f22-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="c8f22-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8f22-110">PARAMETERS</span></span>

### <span data-ttu-id="c8f22-111">-動作</span><span class="sxs-lookup"><span data-stu-id="c8f22-111">-Action</span></span>
<span data-ttu-id="c8f22-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="c8f22-112">Type of Actions.</span></span>
<span data-ttu-id="c8f22-113">可能的值包括： "Allow"，"Block"，"Log"</span><span class="sxs-lookup"><span data-stu-id="c8f22-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f22-114">-DefaultProfile</span></span>
<span data-ttu-id="c8f22-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8f22-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f22-116">-Override</span><span class="sxs-lookup"><span data-stu-id="c8f22-116">-Override</span></span>
<span data-ttu-id="c8f22-117">說明 overrideruleGroup。</span><span class="sxs-lookup"><span data-stu-id="c8f22-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="c8f22-118">可能的值包括： "SqlInjection"、"XSS"</span><span class="sxs-lookup"><span data-stu-id="c8f22-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f22-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f22-119">CommonParameters</span></span>
<span data-ttu-id="c8f22-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8f22-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f22-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8f22-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f22-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c8f22-122">INPUTS</span></span>

### <span data-ttu-id="c8f22-123">所有</span><span class="sxs-lookup"><span data-stu-id="c8f22-123">None</span></span>

## <span data-ttu-id="c8f22-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c8f22-124">OUTPUTS</span></span>

### <span data-ttu-id="c8f22-125">PSAzureRuleGroupOverride 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="c8f22-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="c8f22-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c8f22-126">NOTES</span></span>

## <span data-ttu-id="c8f22-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8f22-127">RELATED LINKS</span></span>

[<span data-ttu-id="c8f22-128">新-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8f22-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
