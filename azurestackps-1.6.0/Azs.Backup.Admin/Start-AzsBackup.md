---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443344"
---
# <span data-ttu-id="813dd-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="813dd-101">Start-AzsBackup</span></span>

## <span data-ttu-id="813dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="813dd-102">SYNOPSIS</span></span>
<span data-ttu-id="813dd-103">備份特定位置。</span><span class="sxs-lookup"><span data-stu-id="813dd-103">Back up a specific location.</span></span>

## <span data-ttu-id="813dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="813dd-104">SYNTAX</span></span>

### <span data-ttu-id="813dd-105">CreateBackup (預設) </span><span class="sxs-lookup"><span data-stu-id="813dd-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="813dd-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="813dd-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="813dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="813dd-107">DESCRIPTION</span></span>
<span data-ttu-id="813dd-108">備份特定位置。</span><span class="sxs-lookup"><span data-stu-id="813dd-108">Back up a specific location.</span></span>

## <span data-ttu-id="813dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="813dd-109">EXAMPLES</span></span>

### <span data-ttu-id="813dd-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="813dd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="813dd-111">啟動 Azure 堆疊備份。</span><span class="sxs-lookup"><span data-stu-id="813dd-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="813dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="813dd-112">PARAMETERS</span></span>

### <span data-ttu-id="813dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="813dd-113">-AsJob</span></span>
<span data-ttu-id="813dd-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="813dd-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="813dd-115">-Force</span></span>
<span data-ttu-id="813dd-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="813dd-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-117">-位置</span><span class="sxs-lookup"><span data-stu-id="813dd-117">-Location</span></span>
<span data-ttu-id="813dd-118">備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="813dd-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="813dd-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="813dd-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="813dd-121">-ResourceId</span></span>
<span data-ttu-id="813dd-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="813dd-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-123">-確認</span><span class="sxs-lookup"><span data-stu-id="813dd-123">-Confirm</span></span>
<span data-ttu-id="813dd-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="813dd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813dd-125">-WhatIf</span></span>
<span data-ttu-id="813dd-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="813dd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="813dd-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="813dd-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813dd-128">CommonParameters</span></span>
<span data-ttu-id="813dd-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="813dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813dd-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="813dd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813dd-131">輸入</span><span class="sxs-lookup"><span data-stu-id="813dd-131">INPUTS</span></span>

## <span data-ttu-id="813dd-132">輸出</span><span class="sxs-lookup"><span data-stu-id="813dd-132">OUTPUTS</span></span>

### <span data-ttu-id="813dd-133">LongRunningOperationStatus 中的 [AzureStack]</span><span class="sxs-lookup"><span data-stu-id="813dd-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="813dd-134">筆記</span><span class="sxs-lookup"><span data-stu-id="813dd-134">NOTES</span></span>

## <span data-ttu-id="813dd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="813dd-135">RELATED LINKS</span></span>

