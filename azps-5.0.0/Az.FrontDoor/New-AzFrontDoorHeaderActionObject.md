---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138863"
---
# <span data-ttu-id="05f7d-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="05f7d-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="05f7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="05f7d-103">建立 PSHeaderAction 物件。</span><span class="sxs-lookup"><span data-stu-id="05f7d-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="05f7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="05f7d-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05f7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="05f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="05f7d-106">建立 PSRulesEngineAction 物件的建立 PSHeaderAction 物件。</span><span class="sxs-lookup"><span data-stu-id="05f7d-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="05f7d-107">示例</span><span class="sxs-lookup"><span data-stu-id="05f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="05f7d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="05f7d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="05f7d-109">參數</span><span class="sxs-lookup"><span data-stu-id="05f7d-109">PARAMETERS</span></span>

### <span data-ttu-id="05f7d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f7d-110">-DefaultProfile</span></span>
<span data-ttu-id="05f7d-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05f7d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05f7d-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="05f7d-112">-HeaderActionType</span></span>
<span data-ttu-id="05f7d-113">要套用至頁首的操作類型。</span><span class="sxs-lookup"><span data-stu-id="05f7d-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="05f7d-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="05f7d-114">-HeaderName</span></span>
<span data-ttu-id="05f7d-115">此動作將套用至的頁首名稱。</span><span class="sxs-lookup"><span data-stu-id="05f7d-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="05f7d-116">-值</span><span class="sxs-lookup"><span data-stu-id="05f7d-116">-Value</span></span>
<span data-ttu-id="05f7d-117">要用來更新指定標頭名稱的值。</span><span class="sxs-lookup"><span data-stu-id="05f7d-117">The value to update the given header name with.</span></span>
<span data-ttu-id="05f7d-118">如果 actionType 是 [刪除]，則不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="05f7d-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="05f7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f7d-119">CommonParameters</span></span>
<span data-ttu-id="05f7d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05f7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f7d-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="05f7d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f7d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="05f7d-122">INPUTS</span></span>

### <span data-ttu-id="05f7d-123">所有</span><span class="sxs-lookup"><span data-stu-id="05f7d-123">None</span></span>

## <span data-ttu-id="05f7d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="05f7d-124">OUTPUTS</span></span>

### <span data-ttu-id="05f7d-125">PSHeaderAction 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="05f7d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="05f7d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="05f7d-126">NOTES</span></span>

## <span data-ttu-id="05f7d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="05f7d-127">RELATED LINKS</span></span>
