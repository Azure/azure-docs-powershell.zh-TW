---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: e25cbbeb4f9920e468638bbae2ef8c53ca241fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623678"
---
# <span data-ttu-id="f92e9-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f92e9-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="f92e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f92e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f92e9-103">針對備份受保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="f92e9-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f92e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f92e9-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f92e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="f92e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f92e9-106">**Disable AzureRmBackupProtection** Cmdlet 會針對 Azure 備份受保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="f92e9-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="f92e9-107">這個 Cmdlet 會停止定期排程的專案備份。</span><span class="sxs-lookup"><span data-stu-id="f92e9-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="f92e9-108">這個 Cmdlet 可以刪除備份專案的現有復原點。</span><span class="sxs-lookup"><span data-stu-id="f92e9-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="f92e9-109">示例</span><span class="sxs-lookup"><span data-stu-id="f92e9-109">EXAMPLES</span></span>

## <span data-ttu-id="f92e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="f92e9-110">PARAMETERS</span></span>

### <span data-ttu-id="f92e9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f92e9-111">-Force</span></span>
<span data-ttu-id="f92e9-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f92e9-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92e9-113">-專案</span><span class="sxs-lookup"><span data-stu-id="f92e9-113">-Item</span></span>
<span data-ttu-id="f92e9-114">指定此 Cmdlet 停用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="f92e9-114">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="f92e9-115">若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f92e9-115">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e9-116">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="f92e9-116">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="f92e9-117">表示此 Cmdlet 會刪除現有的復原點。</span><span class="sxs-lookup"><span data-stu-id="f92e9-117">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="f92e9-118">若要稍後刪除儲存的復原點，請再次執行此 Cmdlet，並指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f92e9-118">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92e9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f92e9-119">-Confirm</span></span>
<span data-ttu-id="f92e9-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f92e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92e9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f92e9-121">-WhatIf</span></span>
<span data-ttu-id="f92e9-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f92e9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f92e9-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f92e9-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92e9-124">-DefaultProfile</span></span>
<span data-ttu-id="f92e9-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f92e9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92e9-126">CommonParameters</span></span>
<span data-ttu-id="f92e9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f92e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92e9-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f92e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92e9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f92e9-129">INPUTS</span></span>

### <span data-ttu-id="f92e9-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f92e9-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="f92e9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f92e9-131">OUTPUTS</span></span>

### <span data-ttu-id="f92e9-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f92e9-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="f92e9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f92e9-133">NOTES</span></span>

## <span data-ttu-id="f92e9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f92e9-134">RELATED LINKS</span></span>

[<span data-ttu-id="f92e9-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f92e9-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="f92e9-136">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f92e9-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


