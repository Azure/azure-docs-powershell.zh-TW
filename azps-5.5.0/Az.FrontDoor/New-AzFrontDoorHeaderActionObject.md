---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140887"
---
# <span data-ttu-id="f3ce1-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="f3ce1-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="f3ce1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ce1-103">建立 PSHeaderAction 物件。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="f3ce1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3ce1-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3ce1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ce1-106">建立 PSRulesEngineAction 物件的建立 PSHeaderAction 物件。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="f3ce1-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ce1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f3ce1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="f3ce1-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3ce1-109">PARAMETERS</span></span>

### <span data-ttu-id="f3ce1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ce1-110">-DefaultProfile</span></span>
<span data-ttu-id="f3ce1-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ce1-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="f3ce1-112">-HeaderActionType</span></span>
<span data-ttu-id="f3ce1-113">要套用至頁首的操作類型。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce1-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="f3ce1-114">-HeaderName</span></span>
<span data-ttu-id="f3ce1-115">此動作將套用至的頁首名稱。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce1-116">-值</span><span class="sxs-lookup"><span data-stu-id="f3ce1-116">-Value</span></span>
<span data-ttu-id="f3ce1-117">要用來更新指定標頭名稱的值。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-117">The value to update the given header name with.</span></span>
<span data-ttu-id="f3ce1-118">如果 actionType 是 [刪除]，則不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ce1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ce1-119">CommonParameters</span></span>
<span data-ttu-id="f3ce1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ce1-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ce1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f3ce1-122">INPUTS</span></span>

### <span data-ttu-id="f3ce1-123">所有</span><span class="sxs-lookup"><span data-stu-id="f3ce1-123">None</span></span>

## <span data-ttu-id="f3ce1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f3ce1-124">OUTPUTS</span></span>

### <span data-ttu-id="f3ce1-125">PSHeaderAction 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="f3ce1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="f3ce1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f3ce1-126">NOTES</span></span>

## <span data-ttu-id="f3ce1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3ce1-127">RELATED LINKS</span></span>
