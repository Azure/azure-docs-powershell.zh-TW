---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b30ae24d384667aa8d399f03c76ab886b2faa1c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442703"
---
# <span data-ttu-id="7d567-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="7d567-101">New-DataDiskObject</span></span>

## <span data-ttu-id="7d567-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d567-102">SYNOPSIS</span></span>
<span data-ttu-id="7d567-103">建立用來建立新的虛擬機器平臺影像的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7d567-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="7d567-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d567-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d567-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d567-105">DESCRIPTION</span></span>
<span data-ttu-id="7d567-106">建立擁有資料磁片相關資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="7d567-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="7d567-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d567-107">EXAMPLES</span></span>

### <span data-ttu-id="7d567-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d567-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="7d567-109">建立新的資料磁片盤物件。</span><span class="sxs-lookup"><span data-stu-id="7d567-109">Create a new data disk object.</span></span>

## <span data-ttu-id="7d567-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d567-110">PARAMETERS</span></span>

### <span data-ttu-id="7d567-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="7d567-111">-Lun</span></span>
<span data-ttu-id="7d567-112">邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="7d567-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d567-113">-Uri</span><span class="sxs-lookup"><span data-stu-id="7d567-113">-Uri</span></span>
<span data-ttu-id="7d567-114">磁片模版的位置。</span><span class="sxs-lookup"><span data-stu-id="7d567-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="7d567-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d567-115">CommonParameters</span></span>
<span data-ttu-id="7d567-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d567-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d567-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d567-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d567-118">輸入</span><span class="sxs-lookup"><span data-stu-id="7d567-118">INPUTS</span></span>

## <span data-ttu-id="7d567-119">輸出</span><span class="sxs-lookup"><span data-stu-id="7d567-119">OUTPUTS</span></span>

## <span data-ttu-id="7d567-120">筆記</span><span class="sxs-lookup"><span data-stu-id="7d567-120">NOTES</span></span>

## <span data-ttu-id="7d567-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d567-121">RELATED LINKS</span></span>
