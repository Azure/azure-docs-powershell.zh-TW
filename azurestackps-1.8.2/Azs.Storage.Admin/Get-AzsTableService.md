---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf6664023fbd43601c9b7c41a4f578809a9717c5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968322"
---
# <span data-ttu-id="54de5-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="54de5-101">Get-AzsTableService</span></span>

## <span data-ttu-id="54de5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54de5-102">SYNOPSIS</span></span>
<span data-ttu-id="54de5-103">傳回資料表服務。</span><span class="sxs-lookup"><span data-stu-id="54de5-103">Returns the table service.</span></span>

## <span data-ttu-id="54de5-104">句法</span><span class="sxs-lookup"><span data-stu-id="54de5-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="54de5-105">說明</span><span class="sxs-lookup"><span data-stu-id="54de5-105">DESCRIPTION</span></span>
<span data-ttu-id="54de5-106">傳回資料表服務。</span><span class="sxs-lookup"><span data-stu-id="54de5-106">Returns the table service.</span></span>

## <span data-ttu-id="54de5-107">示例</span><span class="sxs-lookup"><span data-stu-id="54de5-107">EXAMPLES</span></span>

### <span data-ttu-id="54de5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="54de5-108">EXAMPLE 1</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="54de5-109">取得資料表 servie。</span><span class="sxs-lookup"><span data-stu-id="54de5-109">Get the table servie.</span></span>

## <span data-ttu-id="54de5-110">參數</span><span class="sxs-lookup"><span data-stu-id="54de5-110">PARAMETERS</span></span>

### <span data-ttu-id="54de5-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="54de5-111">-FarmName</span></span>
<span data-ttu-id="54de5-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="54de5-112">Farm Id.</span></span>

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

### <span data-ttu-id="54de5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54de5-113">-ResourceGroupName</span></span>
<span data-ttu-id="54de5-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="54de5-114">Resource group name.</span></span>

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

### <span data-ttu-id="54de5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54de5-115">CommonParameters</span></span>
<span data-ttu-id="54de5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54de5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54de5-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54de5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54de5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="54de5-118">INPUTS</span></span>

## <span data-ttu-id="54de5-119">輸出</span><span class="sxs-lookup"><span data-stu-id="54de5-119">OUTPUTS</span></span>

### <span data-ttu-id="54de5-120">AzureStack （TableService）的</span><span class="sxs-lookup"><span data-stu-id="54de5-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="54de5-121">筆記</span><span class="sxs-lookup"><span data-stu-id="54de5-121">NOTES</span></span>

## <span data-ttu-id="54de5-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="54de5-122">RELATED LINKS</span></span>
