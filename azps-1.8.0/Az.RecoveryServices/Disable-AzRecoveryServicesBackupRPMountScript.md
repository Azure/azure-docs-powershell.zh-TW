---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 934f7ac105ee1164011df9bcacc672437ef4bf78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621206"
---
# <span data-ttu-id="6199e-101">Disable-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="6199e-101">Disable-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="6199e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6199e-102">SYNOPSIS</span></span>
<span data-ttu-id="6199e-103">卸載復原點的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="6199e-103">Dismounts all the files of the recovery point.</span></span>

## <span data-ttu-id="6199e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6199e-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6199e-105">說明</span><span class="sxs-lookup"><span data-stu-id="6199e-105">DESCRIPTION</span></span>
<span data-ttu-id="6199e-106">Disable-AzRecoveryServicesBackupRPMountScript Cmdlet 會卸載先前使用 Get-AzRecoveryServicesBackupRPMountScript Cmdlet 裝載的復原點檔案。</span><span class="sxs-lookup"><span data-stu-id="6199e-106">The Disable-AzRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="6199e-107">示例</span><span class="sxs-lookup"><span data-stu-id="6199e-107">EXAMPLES</span></span>

### <span data-ttu-id="6199e-108">範例1：卸載復原點</span><span class="sxs-lookup"><span data-stu-id="6199e-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="6199e-109">參數</span><span class="sxs-lookup"><span data-stu-id="6199e-109">PARAMETERS</span></span>

### <span data-ttu-id="6199e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6199e-110">-DefaultProfile</span></span>
<span data-ttu-id="6199e-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6199e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6199e-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6199e-112">-PassThru</span></span>
<span data-ttu-id="6199e-113">傳回復原點。</span><span class="sxs-lookup"><span data-stu-id="6199e-113">Return the recovery point.</span></span>

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

### <span data-ttu-id="6199e-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6199e-114">-RecoveryPoint</span></span>
<span data-ttu-id="6199e-115">要還原的復原點物件</span><span class="sxs-lookup"><span data-stu-id="6199e-115">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6199e-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6199e-116">-VaultId</span></span>
<span data-ttu-id="6199e-117">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="6199e-117">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6199e-118">-確認</span><span class="sxs-lookup"><span data-stu-id="6199e-118">-Confirm</span></span>
<span data-ttu-id="6199e-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6199e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6199e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6199e-120">-WhatIf</span></span>
<span data-ttu-id="6199e-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6199e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6199e-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6199e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6199e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6199e-123">CommonParameters</span></span>
<span data-ttu-id="6199e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6199e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6199e-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6199e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6199e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6199e-126">INPUTS</span></span>

### <span data-ttu-id="6199e-127">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="6199e-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="6199e-128">System.object</span><span class="sxs-lookup"><span data-stu-id="6199e-128">System.String</span></span>

## <span data-ttu-id="6199e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6199e-129">OUTPUTS</span></span>

### <span data-ttu-id="6199e-130">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="6199e-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="6199e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6199e-131">NOTES</span></span>

## <span data-ttu-id="6199e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6199e-132">RELATED LINKS</span></span>
