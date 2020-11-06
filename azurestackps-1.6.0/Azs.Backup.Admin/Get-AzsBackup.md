---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443359"
---
# <span data-ttu-id="0a839-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="0a839-101">Get-AzsBackup</span></span>

## <span data-ttu-id="0a839-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a839-102">SYNOPSIS</span></span>
<span data-ttu-id="0a839-103">從以名稱為基礎的位置傳回備份。</span><span class="sxs-lookup"><span data-stu-id="0a839-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="0a839-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a839-104">SYNTAX</span></span>

### <span data-ttu-id="0a839-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0a839-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a839-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0a839-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a839-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a839-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="0a839-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="0a839-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0a839-109">說明</span><span class="sxs-lookup"><span data-stu-id="0a839-109">DESCRIPTION</span></span>
<span data-ttu-id="0a839-110">從以名稱為基礎的位置傳回備份。</span><span class="sxs-lookup"><span data-stu-id="0a839-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="0a839-111">示例</span><span class="sxs-lookup"><span data-stu-id="0a839-111">EXAMPLES</span></span>

### <span data-ttu-id="0a839-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a839-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="0a839-113">取得所有 Azure 堆疊備份的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0a839-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="0a839-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a839-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="0a839-115">取得指定 Azure 堆疊備份的資訊。</span><span class="sxs-lookup"><span data-stu-id="0a839-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="0a839-116">參數</span><span class="sxs-lookup"><span data-stu-id="0a839-116">PARAMETERS</span></span>

### <span data-ttu-id="0a839-117">-位置</span><span class="sxs-lookup"><span data-stu-id="0a839-117">-Location</span></span>
<span data-ttu-id="0a839-118">備份位置。</span><span class="sxs-lookup"><span data-stu-id="0a839-118">Location backed up.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a839-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a839-119">-Name</span></span>
<span data-ttu-id="0a839-120">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a839-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a839-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="0a839-121">-ParentResource</span></span>
<span data-ttu-id="0a839-122">傳送備份位置將會傳回該備份位置的所有備份清單。</span><span class="sxs-lookup"><span data-stu-id="0a839-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a839-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a839-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a839-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a839-124">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a839-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a839-125">-ResourceId</span></span>
<span data-ttu-id="0a839-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0a839-126">The resource id.</span></span>

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

### <span data-ttu-id="0a839-127">-略過</span><span class="sxs-lookup"><span data-stu-id="0a839-127">-Skip</span></span>
<span data-ttu-id="0a839-128">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="0a839-128">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a839-129">-上方</span><span class="sxs-lookup"><span data-stu-id="0a839-129">-Top</span></span>
<span data-ttu-id="0a839-130">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="0a839-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0a839-131">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="0a839-131">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a839-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a839-132">CommonParameters</span></span>
<span data-ttu-id="0a839-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a839-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a839-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a839-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a839-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0a839-135">INPUTS</span></span>

## <span data-ttu-id="0a839-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0a839-136">OUTPUTS</span></span>

### <span data-ttu-id="0a839-137">AzureStack. 備份. 管理模型. 備份</span><span class="sxs-lookup"><span data-stu-id="0a839-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="0a839-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0a839-138">NOTES</span></span>

## <span data-ttu-id="0a839-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a839-139">RELATED LINKS</span></span>

