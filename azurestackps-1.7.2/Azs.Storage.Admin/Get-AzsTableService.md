---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01b3c055873276a265859683e07cd9150ffedafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793050"
---
# <span data-ttu-id="8ba89-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="8ba89-101">Get-AzsTableService</span></span>

## <span data-ttu-id="8ba89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ba89-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba89-103">傳回資料表服務。</span><span class="sxs-lookup"><span data-stu-id="8ba89-103">Returns the table service.</span></span>

## <span data-ttu-id="8ba89-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ba89-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ba89-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ba89-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba89-106">傳回資料表服務。</span><span class="sxs-lookup"><span data-stu-id="8ba89-106">Returns the table service.</span></span>

## <span data-ttu-id="8ba89-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ba89-107">EXAMPLES</span></span>

### <span data-ttu-id="8ba89-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ba89-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="8ba89-109">取得資料表 servie。</span><span class="sxs-lookup"><span data-stu-id="8ba89-109">Get the table servie.</span></span>

## <span data-ttu-id="8ba89-110">參數</span><span class="sxs-lookup"><span data-stu-id="8ba89-110">PARAMETERS</span></span>

### <span data-ttu-id="8ba89-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8ba89-111">-FarmName</span></span>
<span data-ttu-id="8ba89-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="8ba89-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba89-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba89-113">-ResourceGroupName</span></span>
<span data-ttu-id="8ba89-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba89-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba89-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba89-115">CommonParameters</span></span>
<span data-ttu-id="8ba89-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ba89-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba89-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ba89-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba89-118">輸入</span><span class="sxs-lookup"><span data-stu-id="8ba89-118">INPUTS</span></span>

## <span data-ttu-id="8ba89-119">輸出</span><span class="sxs-lookup"><span data-stu-id="8ba89-119">OUTPUTS</span></span>

### <span data-ttu-id="8ba89-120">AzureStack （TableService）的</span><span class="sxs-lookup"><span data-stu-id="8ba89-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="8ba89-121">筆記</span><span class="sxs-lookup"><span data-stu-id="8ba89-121">NOTES</span></span>

## <span data-ttu-id="8ba89-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ba89-122">RELATED LINKS</span></span>

