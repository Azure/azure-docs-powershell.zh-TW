---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968225"
---
# <span data-ttu-id="099fe-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="099fe-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="099fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="099fe-102">SYNOPSIS</span></span>
<span data-ttu-id="099fe-103">取消受管理的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="099fe-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="099fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="099fe-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="099fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="099fe-105">DESCRIPTION</span></span>
<span data-ttu-id="099fe-106">取消磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="099fe-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="099fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="099fe-107">EXAMPLES</span></span>

### <span data-ttu-id="099fe-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="099fe-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="099fe-109">取消受管理的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="099fe-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="099fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="099fe-110">PARAMETERS</span></span>

### <span data-ttu-id="099fe-111">-位置</span><span class="sxs-lookup"><span data-stu-id="099fe-111">-Location</span></span>
<span data-ttu-id="099fe-112">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="099fe-112">Location of the resource.</span></span>

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

### <span data-ttu-id="099fe-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="099fe-113">-Name</span></span>
<span data-ttu-id="099fe-114">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="099fe-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="099fe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099fe-115">CommonParameters</span></span>
<span data-ttu-id="099fe-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="099fe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099fe-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="099fe-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099fe-118">輸入</span><span class="sxs-lookup"><span data-stu-id="099fe-118">INPUTS</span></span>

## <span data-ttu-id="099fe-119">輸出</span><span class="sxs-lookup"><span data-stu-id="099fe-119">OUTPUTS</span></span>

### <span data-ttu-id="099fe-120">AzureStack （DiskMigrationJob）的計算。</span><span class="sxs-lookup"><span data-stu-id="099fe-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="099fe-121">筆記</span><span class="sxs-lookup"><span data-stu-id="099fe-121">NOTES</span></span>

## <span data-ttu-id="099fe-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="099fe-122">RELATED LINKS</span></span>

