---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1f3a965d287aa266683636b4b17a8d8954cace8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793215"
---
# <span data-ttu-id="d4da7-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4da7-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="d4da7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4da7-102">SYNOPSIS</span></span>
<span data-ttu-id="d4da7-103">傳回備份配置清單。</span><span class="sxs-lookup"><span data-stu-id="d4da7-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="d4da7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4da7-104">SYNTAX</span></span>

### <span data-ttu-id="d4da7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="d4da7-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d4da7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="d4da7-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d4da7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4da7-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d4da7-108">說明</span><span class="sxs-lookup"><span data-stu-id="d4da7-108">DESCRIPTION</span></span>
<span data-ttu-id="d4da7-109">傳回備份配置清單。</span><span class="sxs-lookup"><span data-stu-id="d4da7-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="d4da7-110">示例</span><span class="sxs-lookup"><span data-stu-id="d4da7-110">EXAMPLES</span></span>

### <span data-ttu-id="d4da7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d4da7-111">EXAMPLE 1</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="d4da7-112">取得 Azure 堆疊備份設定。</span><span class="sxs-lookup"><span data-stu-id="d4da7-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="d4da7-113">參數</span><span class="sxs-lookup"><span data-stu-id="d4da7-113">PARAMETERS</span></span>

### <span data-ttu-id="d4da7-114">-位置</span><span class="sxs-lookup"><span data-stu-id="d4da7-114">-Location</span></span>
<span data-ttu-id="d4da7-115">備份位置。</span><span class="sxs-lookup"><span data-stu-id="d4da7-115">Backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4da7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4da7-116">-ResourceGroupName</span></span>
<span data-ttu-id="d4da7-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4da7-117">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4da7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4da7-118">-ResourceId</span></span>
<span data-ttu-id="d4da7-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d4da7-119">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4da7-120">-上方</span><span class="sxs-lookup"><span data-stu-id="d4da7-120">-Top</span></span>
<span data-ttu-id="d4da7-121">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="d4da7-121">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d4da7-122">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="d4da7-122">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4da7-123">-略過</span><span class="sxs-lookup"><span data-stu-id="d4da7-123">-Skip</span></span>
<span data-ttu-id="d4da7-124">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="d4da7-124">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4da7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4da7-125">CommonParameters</span></span>
<span data-ttu-id="d4da7-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4da7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4da7-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4da7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4da7-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d4da7-128">INPUTS</span></span>

## <span data-ttu-id="d4da7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d4da7-129">OUTPUTS</span></span>

### <span data-ttu-id="d4da7-130">BackupLocation 中的 [AzureStack]</span><span class="sxs-lookup"><span data-stu-id="d4da7-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="d4da7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d4da7-131">NOTES</span></span>

## <span data-ttu-id="d4da7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4da7-132">RELATED LINKS</span></span>
