---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: ad005dbf386bc8340fa0da0c5e8dac1d11bf4bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906681"
---
# <span data-ttu-id="ed572-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="ed572-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="ed572-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed572-102">SYNOPSIS</span></span>
<span data-ttu-id="ed572-103">建立 PSHeaderAction 物件。</span><span class="sxs-lookup"><span data-stu-id="ed572-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="ed572-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed572-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed572-105">描述</span><span class="sxs-lookup"><span data-stu-id="ed572-105">DESCRIPTION</span></span>
<span data-ttu-id="ed572-106">建立 PSHeaderAction 物件以建立 PSRulesEngineAction 物件。</span><span class="sxs-lookup"><span data-stu-id="ed572-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="ed572-107">例子</span><span class="sxs-lookup"><span data-stu-id="ed572-107">EXAMPLES</span></span>

### <span data-ttu-id="ed572-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ed572-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="ed572-109">參數</span><span class="sxs-lookup"><span data-stu-id="ed572-109">PARAMETERS</span></span>

### <span data-ttu-id="ed572-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed572-110">-DefaultProfile</span></span>
<span data-ttu-id="ed572-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed572-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed572-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="ed572-112">-HeaderActionType</span></span>
<span data-ttu-id="ed572-113">要適用于頁眉的操控類型。</span><span class="sxs-lookup"><span data-stu-id="ed572-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="ed572-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="ed572-114">-HeaderName</span></span>
<span data-ttu-id="ed572-115">此動作將適用于的標題名稱。</span><span class="sxs-lookup"><span data-stu-id="ed572-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="ed572-116">-值</span><span class="sxs-lookup"><span data-stu-id="ed572-116">-Value</span></span>
<span data-ttu-id="ed572-117">這是要更新指定頁眉名稱的值。</span><span class="sxs-lookup"><span data-stu-id="ed572-117">The value to update the given header name with.</span></span>
<span data-ttu-id="ed572-118">如果 actionType 為 Delete，則不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="ed572-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="ed572-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed572-119">CommonParameters</span></span>
<span data-ttu-id="ed572-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed572-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed572-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed572-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed572-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ed572-122">INPUTS</span></span>

### <span data-ttu-id="ed572-123">沒有</span><span class="sxs-lookup"><span data-stu-id="ed572-123">None</span></span>

## <span data-ttu-id="ed572-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ed572-124">OUTPUTS</span></span>

### <span data-ttu-id="ed572-125">Microsoft.Azure.Commands.FrontDoor.models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="ed572-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="ed572-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ed572-126">NOTES</span></span>

## <span data-ttu-id="ed572-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed572-127">RELATED LINKS</span></span>
