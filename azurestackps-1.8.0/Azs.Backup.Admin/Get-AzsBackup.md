---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793693"
---
# <span data-ttu-id="46677-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="46677-101">Get-AzsBackup</span></span>

## <span data-ttu-id="46677-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46677-102">SYNOPSIS</span></span>
<span data-ttu-id="46677-103">從以名稱為基礎的位置傳回備份。</span><span class="sxs-lookup"><span data-stu-id="46677-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="46677-104">句法</span><span class="sxs-lookup"><span data-stu-id="46677-104">SYNTAX</span></span>

### <span data-ttu-id="46677-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="46677-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="46677-106">獲取</span><span class="sxs-lookup"><span data-stu-id="46677-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="46677-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46677-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="46677-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="46677-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="46677-109">說明</span><span class="sxs-lookup"><span data-stu-id="46677-109">DESCRIPTION</span></span>
<span data-ttu-id="46677-110">從以名稱為基礎的位置傳回備份。</span><span class="sxs-lookup"><span data-stu-id="46677-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="46677-111">示例</span><span class="sxs-lookup"><span data-stu-id="46677-111">EXAMPLES</span></span>

### <span data-ttu-id="46677-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46677-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="46677-113">取得所有 Azure 堆疊備份的資訊 sbout。</span><span class="sxs-lookup"><span data-stu-id="46677-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="46677-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="46677-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="46677-115">取得指定 Azure 堆疊備份的資訊。</span><span class="sxs-lookup"><span data-stu-id="46677-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="46677-116">參數</span><span class="sxs-lookup"><span data-stu-id="46677-116">PARAMETERS</span></span>

### <span data-ttu-id="46677-117">-位置</span><span class="sxs-lookup"><span data-stu-id="46677-117">-Location</span></span>
<span data-ttu-id="46677-118">備份位置。</span><span class="sxs-lookup"><span data-stu-id="46677-118">Location backed up.</span></span>

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

### <span data-ttu-id="46677-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="46677-119">-Name</span></span>
<span data-ttu-id="46677-120">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="46677-120">Name of the backup.</span></span>

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

### <span data-ttu-id="46677-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="46677-121">-ParentResource</span></span>
<span data-ttu-id="46677-122">傳送備份位置將會傳回該備份位置的所有備份清單。</span><span class="sxs-lookup"><span data-stu-id="46677-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="46677-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46677-123">-ResourceGroupName</span></span>
<span data-ttu-id="46677-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46677-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="46677-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46677-125">-ResourceId</span></span>
<span data-ttu-id="46677-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="46677-126">The resource id.</span></span>

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

### <span data-ttu-id="46677-127">-略過</span><span class="sxs-lookup"><span data-stu-id="46677-127">-Skip</span></span>
<span data-ttu-id="46677-128">{{Fill 略過說明}}</span><span class="sxs-lookup"><span data-stu-id="46677-128">{{Fill Skip Description}}</span></span>

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

### <span data-ttu-id="46677-129">-上方</span><span class="sxs-lookup"><span data-stu-id="46677-129">-Top</span></span>
<span data-ttu-id="46677-130">{{Fill Top 說明}}</span><span class="sxs-lookup"><span data-stu-id="46677-130">{{Fill Top Description}}</span></span>

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

### <span data-ttu-id="46677-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46677-131">CommonParameters</span></span>
<span data-ttu-id="46677-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46677-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46677-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46677-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46677-134">輸入</span><span class="sxs-lookup"><span data-stu-id="46677-134">INPUTS</span></span>

## <span data-ttu-id="46677-135">輸出</span><span class="sxs-lookup"><span data-stu-id="46677-135">OUTPUTS</span></span>

### <span data-ttu-id="46677-136">AzureStack. 備份. 管理模型. 備份</span><span class="sxs-lookup"><span data-stu-id="46677-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="46677-137">筆記</span><span class="sxs-lookup"><span data-stu-id="46677-137">NOTES</span></span>

## <span data-ttu-id="46677-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="46677-138">RELATED LINKS</span></span>

