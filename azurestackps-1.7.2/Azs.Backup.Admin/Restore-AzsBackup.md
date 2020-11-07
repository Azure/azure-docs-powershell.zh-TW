---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "93799350"
---
# <span data-ttu-id="622c0-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="622c0-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="622c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="622c0-102">SYNOPSIS</span></span>
<span data-ttu-id="622c0-103">還原備份。</span><span class="sxs-lookup"><span data-stu-id="622c0-103">Restore a backup.</span></span>

## <span data-ttu-id="622c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="622c0-104">SYNTAX</span></span>

### <span data-ttu-id="622c0-105">Backups_Restore (預設) </span><span class="sxs-lookup"><span data-stu-id="622c0-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="622c0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="622c0-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622c0-107">說明</span><span class="sxs-lookup"><span data-stu-id="622c0-107">DESCRIPTION</span></span>
<span data-ttu-id="622c0-108">還原備份。</span><span class="sxs-lookup"><span data-stu-id="622c0-108">Restore a backup.</span></span>

## <span data-ttu-id="622c0-109">示例</span><span class="sxs-lookup"><span data-stu-id="622c0-109">EXAMPLES</span></span>

### <span data-ttu-id="622c0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="622c0-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="622c0-111">從 Azure 堆疊備份還原。</span><span class="sxs-lookup"><span data-stu-id="622c0-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="622c0-112">參數</span><span class="sxs-lookup"><span data-stu-id="622c0-112">PARAMETERS</span></span>

### <span data-ttu-id="622c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="622c0-113">-AsJob</span></span>
<span data-ttu-id="622c0-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="622c0-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="622c0-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="622c0-116">解密證書的密碼。</span><span class="sxs-lookup"><span data-stu-id="622c0-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="622c0-117">-DecryptionCertPath</span></span>
<span data-ttu-id="622c0-118">解密憑證檔案的路徑，其私密金鑰 ( .pfx) 。</span><span class="sxs-lookup"><span data-stu-id="622c0-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="622c0-119">-Force</span></span>
<span data-ttu-id="622c0-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="622c0-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-121">-位置</span><span class="sxs-lookup"><span data-stu-id="622c0-121">-Location</span></span>
<span data-ttu-id="622c0-122">要備份之位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="622c0-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="622c0-123">-Name</span></span>
<span data-ttu-id="622c0-124">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="622c0-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="622c0-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="622c0-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="622c0-127">-ResourceId</span></span>
<span data-ttu-id="622c0-128">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="622c0-128">The resource id.</span></span>

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

### <span data-ttu-id="622c0-129">-確認</span><span class="sxs-lookup"><span data-stu-id="622c0-129">-Confirm</span></span>
<span data-ttu-id="622c0-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="622c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622c0-131">-WhatIf</span></span>
<span data-ttu-id="622c0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="622c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="622c0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="622c0-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622c0-134">CommonParameters</span></span>
<span data-ttu-id="622c0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="622c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622c0-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="622c0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622c0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="622c0-137">INPUTS</span></span>

## <span data-ttu-id="622c0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="622c0-138">OUTPUTS</span></span>

## <span data-ttu-id="622c0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="622c0-139">NOTES</span></span>

## <span data-ttu-id="622c0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="622c0-140">RELATED LINKS</span></span>
