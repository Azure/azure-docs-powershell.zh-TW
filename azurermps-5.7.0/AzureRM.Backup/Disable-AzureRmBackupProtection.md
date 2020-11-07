---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: cd3f5520b688d5a83cae20216fac47e9120b4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625030"
---
# <span data-ttu-id="623ad-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="623ad-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="623ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="623ad-102">SYNOPSIS</span></span>
<span data-ttu-id="623ad-103">針對備份受保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="623ad-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="623ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="623ad-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="623ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="623ad-105">DESCRIPTION</span></span>
<span data-ttu-id="623ad-106">**Disable AzureRmBackupProtection** Cmdlet 會針對 Azure 備份受保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="623ad-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="623ad-107">這個 Cmdlet 會停止定期排程的專案備份。</span><span class="sxs-lookup"><span data-stu-id="623ad-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="623ad-108">這個 Cmdlet 可以刪除備份專案的現有復原點。</span><span class="sxs-lookup"><span data-stu-id="623ad-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="623ad-109">示例</span><span class="sxs-lookup"><span data-stu-id="623ad-109">EXAMPLES</span></span>

## <span data-ttu-id="623ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="623ad-110">PARAMETERS</span></span>

### <span data-ttu-id="623ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623ad-111">-DefaultProfile</span></span>
<span data-ttu-id="623ad-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="623ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ad-113">-Force</span><span class="sxs-lookup"><span data-stu-id="623ad-113">-Force</span></span>
<span data-ttu-id="623ad-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="623ad-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ad-115">-專案</span><span class="sxs-lookup"><span data-stu-id="623ad-115">-Item</span></span>
<span data-ttu-id="623ad-116">指定此 Cmdlet 停用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="623ad-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="623ad-117">若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="623ad-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623ad-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="623ad-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="623ad-119">表示此 Cmdlet 會刪除現有的復原點。</span><span class="sxs-lookup"><span data-stu-id="623ad-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="623ad-120">若要稍後刪除儲存的復原點，請再次執行此 Cmdlet，並指定此參數。</span><span class="sxs-lookup"><span data-stu-id="623ad-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ad-121">-確認</span><span class="sxs-lookup"><span data-stu-id="623ad-121">-Confirm</span></span>
<span data-ttu-id="623ad-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="623ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623ad-123">-WhatIf</span></span>
<span data-ttu-id="623ad-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="623ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="623ad-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="623ad-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623ad-126">CommonParameters</span></span>
<span data-ttu-id="623ad-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="623ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623ad-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="623ad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623ad-129">輸入</span><span class="sxs-lookup"><span data-stu-id="623ad-129">INPUTS</span></span>

### <span data-ttu-id="623ad-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="623ad-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="623ad-131">輸出</span><span class="sxs-lookup"><span data-stu-id="623ad-131">OUTPUTS</span></span>

### <span data-ttu-id="623ad-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="623ad-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="623ad-133">筆記</span><span class="sxs-lookup"><span data-stu-id="623ad-133">NOTES</span></span>

## <span data-ttu-id="623ad-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="623ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="623ad-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="623ad-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="623ad-136">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="623ad-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


