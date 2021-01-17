---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsCheckNameRequestObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsCheckNameRequestObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsCheckNameRequestObject.md
ms.openlocfilehash: 1e4f376099b0fc2c2bb5ef673438497bc9661153
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286256"
---
# <span data-ttu-id="8de3f-101">New-AzDigitalTwinsCheckNameRequestObject</span><span class="sxs-lookup"><span data-stu-id="8de3f-101">New-AzDigitalTwinsCheckNameRequestObject</span></span>

## <span data-ttu-id="8de3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8de3f-102">SYNOPSIS</span></span>
<span data-ttu-id="8de3f-103">為 CheckNameRequest 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="8de3f-103">Create a in-memory object for CheckNameRequest</span></span>

## <span data-ttu-id="8de3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8de3f-104">SYNTAX</span></span>

```
New-AzDigitalTwinsCheckNameRequestObject -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="8de3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8de3f-105">DESCRIPTION</span></span>
<span data-ttu-id="8de3f-106">為 CheckNameRequest 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="8de3f-106">Create a in-memory object for CheckNameRequest</span></span>

## <span data-ttu-id="8de3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8de3f-107">EXAMPLES</span></span>

### <span data-ttu-id="8de3f-108">範例1：依名稱建立 DigitalTwinsCheckNameRequestObject</span><span class="sxs-lookup"><span data-stu-id="8de3f-108">Example 1: Create a DigitalTwinsCheckNameRequestObject by name</span></span>
```powershell
PS C:\> New-AzDigitalTwinsCheckNameRequestObject -name youriTestName

Name          Type
----          ----
youriTestName Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="8de3f-109">依名稱建立 DigitalTwinsCheckNameRequestObject</span><span class="sxs-lookup"><span data-stu-id="8de3f-109">Create a DigitalTwinsCheckNameRequestObject by name</span></span>

## <span data-ttu-id="8de3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="8de3f-110">PARAMETERS</span></span>

### <span data-ttu-id="8de3f-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="8de3f-111">-Name</span></span>
<span data-ttu-id="8de3f-112">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8de3f-112">Resource name.</span></span>

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

### <span data-ttu-id="8de3f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de3f-113">CommonParameters</span></span>
<span data-ttu-id="8de3f-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8de3f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de3f-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8de3f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de3f-116">輸入</span><span class="sxs-lookup"><span data-stu-id="8de3f-116">INPUTS</span></span>

## <span data-ttu-id="8de3f-117">輸出</span><span class="sxs-lookup"><span data-stu-id="8de3f-117">OUTPUTS</span></span>

### <span data-ttu-id="8de3f-118">CheckNameRequest （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="8de3f-118">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.CheckNameRequest</span></span>

## <span data-ttu-id="8de3f-119">筆記</span><span class="sxs-lookup"><span data-stu-id="8de3f-119">NOTES</span></span>

<span data-ttu-id="8de3f-120">別名</span><span class="sxs-lookup"><span data-stu-id="8de3f-120">ALIASES</span></span>

## <span data-ttu-id="8de3f-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="8de3f-121">RELATED LINKS</span></span>

