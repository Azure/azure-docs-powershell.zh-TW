---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968251"
---
# <span data-ttu-id="9a3c4-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="9a3c4-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="9a3c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3c4-103">還原備份。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-103">Restore a backup.</span></span>

## <span data-ttu-id="9a3c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a3c4-104">SYNTAX</span></span>

### <span data-ttu-id="9a3c4-105">Backups_Restore (預設) </span><span class="sxs-lookup"><span data-stu-id="9a3c4-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a3c4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a3c4-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a3c4-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a3c4-107">DESCRIPTION</span></span>
<span data-ttu-id="9a3c4-108">還原備份。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-108">Restore a backup.</span></span>

## <span data-ttu-id="9a3c4-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a3c4-109">EXAMPLES</span></span>

### <span data-ttu-id="9a3c4-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a3c4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="9a3c4-111">從 Azure 堆疊備份還原。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="9a3c4-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a3c4-112">PARAMETERS</span></span>

### <span data-ttu-id="9a3c4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a3c4-113">-AsJob</span></span>
<span data-ttu-id="9a3c4-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9a3c4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9a3c4-115">-Force</span></span>
<span data-ttu-id="9a3c4-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9a3c4-117">-位置</span><span class="sxs-lookup"><span data-stu-id="9a3c4-117">-Location</span></span>
<span data-ttu-id="9a3c4-118">要備份之位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3c4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a3c4-119">-Name</span></span>
<span data-ttu-id="9a3c4-120">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a3c4-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3c4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a3c4-123">-ResourceId</span></span>
<span data-ttu-id="9a3c4-124">{{Fill ResourceId 描述}}</span><span class="sxs-lookup"><span data-stu-id="9a3c4-124">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3c4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="9a3c4-125">-Confirm</span></span>
<span data-ttu-id="9a3c4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a3c4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a3c4-127">-WhatIf</span></span>
<span data-ttu-id="9a3c4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a3c4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a3c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3c4-130">CommonParameters</span></span>
<span data-ttu-id="9a3c4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3c4-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a3c4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3c4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9a3c4-133">INPUTS</span></span>

## <span data-ttu-id="9a3c4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9a3c4-134">OUTPUTS</span></span>

## <span data-ttu-id="9a3c4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9a3c4-135">NOTES</span></span>

## <span data-ttu-id="9a3c4-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a3c4-136">RELATED LINKS</span></span>

