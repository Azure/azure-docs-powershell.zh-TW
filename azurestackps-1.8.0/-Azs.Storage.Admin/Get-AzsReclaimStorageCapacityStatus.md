---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793722"
---
# <span data-ttu-id="8e3e5-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="8e3e5-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="8e3e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3e5-103">傳回垃圾收集作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="8e3e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e3e5-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e3e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e3e5-105">DESCRIPTION</span></span>
<span data-ttu-id="8e3e5-106">傳回垃圾收集作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="8e3e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="8e3e5-107">EXAMPLES</span></span>

### <span data-ttu-id="8e3e5-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e3e5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="8e3e5-109">傳回垃圾收集狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="8e3e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="8e3e5-110">PARAMETERS</span></span>

### <span data-ttu-id="8e3e5-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8e3e5-111">-FarmName</span></span>
<span data-ttu-id="8e3e5-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-112">Farm Id.</span></span>

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

### <span data-ttu-id="8e3e5-113">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="8e3e5-113">-JobId</span></span>
<span data-ttu-id="8e3e5-114">操作 Id。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="8e3e5-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3e5-117">CommonParameters</span></span>
<span data-ttu-id="8e3e5-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3e5-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e3e5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3e5-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8e3e5-120">INPUTS</span></span>

## <span data-ttu-id="8e3e5-121">輸出</span><span class="sxs-lookup"><span data-stu-id="8e3e5-121">OUTPUTS</span></span>

## <span data-ttu-id="8e3e5-122">筆記</span><span class="sxs-lookup"><span data-stu-id="8e3e5-122">NOTES</span></span>

## <span data-ttu-id="8e3e5-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e3e5-123">RELATED LINKS</span></span>

