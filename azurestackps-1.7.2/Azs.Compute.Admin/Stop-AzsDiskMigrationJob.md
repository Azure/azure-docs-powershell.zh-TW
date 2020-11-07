---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793424"
---
# <span data-ttu-id="cd643-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="cd643-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="cd643-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd643-102">SYNOPSIS</span></span>
<span data-ttu-id="cd643-103">取消受管理的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="cd643-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="cd643-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd643-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="cd643-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd643-105">DESCRIPTION</span></span>
<span data-ttu-id="cd643-106">取消磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="cd643-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="cd643-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd643-107">EXAMPLES</span></span>

### <span data-ttu-id="cd643-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd643-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="cd643-109">取消受管理的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="cd643-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="cd643-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd643-110">PARAMETERS</span></span>

### <span data-ttu-id="cd643-111">-位置</span><span class="sxs-lookup"><span data-stu-id="cd643-111">-Location</span></span>
<span data-ttu-id="cd643-112">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cd643-112">Location of the resource.</span></span>

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

### <span data-ttu-id="cd643-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd643-113">-Name</span></span>
<span data-ttu-id="cd643-114">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="cd643-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd643-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd643-115">CommonParameters</span></span>
<span data-ttu-id="cd643-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd643-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd643-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd643-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd643-118">輸入</span><span class="sxs-lookup"><span data-stu-id="cd643-118">INPUTS</span></span>

## <span data-ttu-id="cd643-119">輸出</span><span class="sxs-lookup"><span data-stu-id="cd643-119">OUTPUTS</span></span>

### <span data-ttu-id="cd643-120">AzureStack （DiskMigrationJob）的計算。</span><span class="sxs-lookup"><span data-stu-id="cd643-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="cd643-121">筆記</span><span class="sxs-lookup"><span data-stu-id="cd643-121">NOTES</span></span>

## <span data-ttu-id="cd643-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd643-122">RELATED LINKS</span></span>

