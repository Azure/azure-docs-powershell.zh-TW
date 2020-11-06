---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6301c621de4399509c70271eb318983e91ebd121
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621143"
---
# <span data-ttu-id="81c18-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="81c18-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="81c18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81c18-102">SYNOPSIS</span></span>
<span data-ttu-id="81c18-103">下載腳本以掛載復原點的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="81c18-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="81c18-104">句法</span><span class="sxs-lookup"><span data-stu-id="81c18-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c18-105">說明</span><span class="sxs-lookup"><span data-stu-id="81c18-105">DESCRIPTION</span></span>
<span data-ttu-id="81c18-106">Get-AzRecoveryServicesBackupRPMountScript Cmdlet 會下載一個腳本，此腳本會在執行此電腦的電腦上掛載復原點的磁片。</span><span class="sxs-lookup"><span data-stu-id="81c18-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="81c18-107">示例</span><span class="sxs-lookup"><span data-stu-id="81c18-107">EXAMPLES</span></span>

### <span data-ttu-id="81c18-108">範例1：裝載復原點</span><span class="sxs-lookup"><span data-stu-id="81c18-108">Example 1: Mount a recovery point</span></span>
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
```

<span data-ttu-id="81c18-109">當腳本執行時，它會將復原點的檔案裝入 $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="81c18-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="81c18-110">參數</span><span class="sxs-lookup"><span data-stu-id="81c18-110">PARAMETERS</span></span>

### <span data-ttu-id="81c18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c18-111">-DefaultProfile</span></span>
<span data-ttu-id="81c18-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81c18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c18-113">-Path</span><span class="sxs-lookup"><span data-stu-id="81c18-113">-Path</span></span>
<span data-ttu-id="81c18-114">檔案恢復的情況下，應該下載檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="81c18-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="81c18-115">如果未提供-Path，腳本檔案將會下載在目前的目錄中。</span><span class="sxs-lookup"><span data-stu-id="81c18-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c18-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="81c18-116">-RecoveryPoint</span></span>
<span data-ttu-id="81c18-117">要還原的復原點物件</span><span class="sxs-lookup"><span data-stu-id="81c18-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="81c18-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="81c18-118">-VaultId</span></span>
<span data-ttu-id="81c18-119">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="81c18-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="81c18-120">-確認</span><span class="sxs-lookup"><span data-stu-id="81c18-120">-Confirm</span></span>
<span data-ttu-id="81c18-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81c18-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c18-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c18-122">-WhatIf</span></span>
<span data-ttu-id="81c18-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81c18-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c18-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81c18-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c18-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c18-125">CommonParameters</span></span>
<span data-ttu-id="81c18-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81c18-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c18-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81c18-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c18-128">輸入</span><span class="sxs-lookup"><span data-stu-id="81c18-128">INPUTS</span></span>

### <span data-ttu-id="81c18-129">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="81c18-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="81c18-130">System.object</span><span class="sxs-lookup"><span data-stu-id="81c18-130">System.String</span></span>

## <span data-ttu-id="81c18-131">輸出</span><span class="sxs-lookup"><span data-stu-id="81c18-131">OUTPUTS</span></span>

### <span data-ttu-id="81c18-132">RPMountScriptDetails 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="81c18-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="81c18-133">筆記</span><span class="sxs-lookup"><span data-stu-id="81c18-133">NOTES</span></span>

## <span data-ttu-id="81c18-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="81c18-134">RELATED LINKS</span></span>