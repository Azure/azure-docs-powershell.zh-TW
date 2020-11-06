---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: bfcd198cd629c9b5f1cd37d3d144bc810a6f4b37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446152"
---
# <span data-ttu-id="b216e-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b216e-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b216e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b216e-102">SYNOPSIS</span></span>
<span data-ttu-id="b216e-103">卸載復原點的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="b216e-103">Dismounts all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b216e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b216e-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b216e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b216e-105">DESCRIPTION</span></span>
<span data-ttu-id="b216e-106">Disable-AzureRmRecoveryServicesBackupRPMountScript Cmdlet 會卸載先前使用 Get-AzureRmRecoveryServicesBackupRPMountScript Cmdlet 裝載的復原點檔案。</span><span class="sxs-lookup"><span data-stu-id="b216e-106">The Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="b216e-107">示例</span><span class="sxs-lookup"><span data-stu-id="b216e-107">EXAMPLES</span></span>

### <span data-ttu-id="b216e-108">範例1：卸載復原點</span><span class="sxs-lookup"><span data-stu-id="b216e-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="b216e-109">參數</span><span class="sxs-lookup"><span data-stu-id="b216e-109">PARAMETERS</span></span>

### <span data-ttu-id="b216e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b216e-110">-DefaultProfile</span></span>
<span data-ttu-id="b216e-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b216e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b216e-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b216e-112">-PassThru</span></span>
<span data-ttu-id="b216e-113">傳回復原點。</span><span class="sxs-lookup"><span data-stu-id="b216e-113">Return the recovery point.</span></span>

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

### <span data-ttu-id="b216e-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b216e-114">-RecoveryPoint</span></span>
<span data-ttu-id="b216e-115">要還原的復原點物件</span><span class="sxs-lookup"><span data-stu-id="b216e-115">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b216e-116">-確認</span><span class="sxs-lookup"><span data-stu-id="b216e-116">-Confirm</span></span>
<span data-ttu-id="b216e-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b216e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b216e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b216e-118">-WhatIf</span></span>
<span data-ttu-id="b216e-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b216e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b216e-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b216e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b216e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b216e-121">CommonParameters</span></span>
<span data-ttu-id="b216e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b216e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b216e-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b216e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b216e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b216e-124">INPUTS</span></span>

### <span data-ttu-id="b216e-125">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="b216e-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b216e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b216e-126">OUTPUTS</span></span>

### <span data-ttu-id="b216e-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b216e-127">System.Object</span></span>

## <span data-ttu-id="b216e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b216e-128">NOTES</span></span>

## <span data-ttu-id="b216e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b216e-129">RELATED LINKS</span></span>

