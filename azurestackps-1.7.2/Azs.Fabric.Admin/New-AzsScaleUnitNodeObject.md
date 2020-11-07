---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792989"
---
# <span data-ttu-id="4322d-101">New-AzsScaleUnitNodeObject</span><span class="sxs-lookup"><span data-stu-id="4322d-101">New-AzsScaleUnitNodeObject</span></span>

## <span data-ttu-id="4322d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4322d-102">SYNOPSIS</span></span>
<span data-ttu-id="4322d-103">輸入可讓您新增 [刻度單位] 節點的資料。</span><span class="sxs-lookup"><span data-stu-id="4322d-103">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="4322d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4322d-104">SYNTAX</span></span>

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4322d-105">說明</span><span class="sxs-lookup"><span data-stu-id="4322d-105">DESCRIPTION</span></span>
<span data-ttu-id="4322d-106">輸入可讓您新增 [刻度單位] 節點的資料。</span><span class="sxs-lookup"><span data-stu-id="4322d-106">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="4322d-107">示例</span><span class="sxs-lookup"><span data-stu-id="4322d-107">EXAMPLES</span></span>

### <span data-ttu-id="4322d-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4322d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

<span data-ttu-id="4322d-109">建立新的 node 物件。</span><span class="sxs-lookup"><span data-stu-id="4322d-109">Create a new node object.</span></span>

## <span data-ttu-id="4322d-110">參數</span><span class="sxs-lookup"><span data-stu-id="4322d-110">PARAMETERS</span></span>

### <span data-ttu-id="4322d-111">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="4322d-111">-BMCIPv4Address</span></span>
<span data-ttu-id="4322d-112">物理電腦的 Bmc 位址。</span><span class="sxs-lookup"><span data-stu-id="4322d-112">Bmc address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4322d-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="4322d-113">-ComputerName</span></span>
<span data-ttu-id="4322d-114">物理電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4322d-114">Computer name of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4322d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4322d-115">CommonParameters</span></span>
<span data-ttu-id="4322d-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4322d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4322d-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4322d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4322d-118">輸入</span><span class="sxs-lookup"><span data-stu-id="4322d-118">INPUTS</span></span>

## <span data-ttu-id="4322d-119">輸出</span><span class="sxs-lookup"><span data-stu-id="4322d-119">OUTPUTS</span></span>

## <span data-ttu-id="4322d-120">筆記</span><span class="sxs-lookup"><span data-stu-id="4322d-120">NOTES</span></span>

## <span data-ttu-id="4322d-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="4322d-121">RELATED LINKS</span></span>

