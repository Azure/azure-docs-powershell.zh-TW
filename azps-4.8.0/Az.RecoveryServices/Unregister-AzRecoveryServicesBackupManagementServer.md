---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: cc52435ff0b288656e4a917620659737f33916ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970806"
---
# <span data-ttu-id="e04d9-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e04d9-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="e04d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e04d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e04d9-103">從保存庫登出 SCDPM 服務器或備份伺服器。</span><span class="sxs-lookup"><span data-stu-id="e04d9-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="e04d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e04d9-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e04d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e04d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e04d9-106">[ **登出 AzRecoveryServicesBackupManagementServer** ] Cmdlet 會從保存庫中登出) 伺服器或 Azure 備份伺服器的系統中心資料保護管理員 (SCDPM。</span><span class="sxs-lookup"><span data-stu-id="e04d9-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="e04d9-107">這個 Cmdlet 會移除未從保存庫中登出之伺服器的參考。</span><span class="sxs-lookup"><span data-stu-id="e04d9-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="e04d9-108">在您可以取消註冊容器之前，您必須刪除所有與該容器相關聯的受保護資料。</span><span class="sxs-lookup"><span data-stu-id="e04d9-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="e04d9-109">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e04d9-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e04d9-110">示例</span><span class="sxs-lookup"><span data-stu-id="e04d9-110">EXAMPLES</span></span>

### <span data-ttu-id="e04d9-111">範例1：從保存庫登出 SCDPM 服務器</span><span class="sxs-lookup"><span data-stu-id="e04d9-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="e04d9-112">第一個命令會取得名為 dpmserver01.contoso.com 的備份管理伺服器，然後將它儲存在 $BMS 變數中。</span><span class="sxs-lookup"><span data-stu-id="e04d9-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="e04d9-113">第二個命令會從保存庫登出 SCDPM 服務器。</span><span class="sxs-lookup"><span data-stu-id="e04d9-113">The second command unregisters the SCDPM server from the vault.</span></span>

### <span data-ttu-id="e04d9-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e04d9-114">Example 2</span></span>

<span data-ttu-id="e04d9-115">從保存庫登出 SCDPM 服務器或備份伺服器。</span><span class="sxs-lookup"><span data-stu-id="e04d9-115">Unregisters a SCDPM server or Backup server from the vault.</span></span> <span data-ttu-id="e04d9-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="e04d9-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## <span data-ttu-id="e04d9-117">參數</span><span class="sxs-lookup"><span data-stu-id="e04d9-117">PARAMETERS</span></span>

### <span data-ttu-id="e04d9-118">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e04d9-118">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="e04d9-119">[恢復服務] 備份容器。</span><span class="sxs-lookup"><span data-stu-id="e04d9-119">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04d9-120">-DefaultProfile</span></span>
<span data-ttu-id="e04d9-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e04d9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e04d9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e04d9-122">-PassThru</span></span>
<span data-ttu-id="e04d9-123">傳回要刪除的備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="e04d9-123">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="e04d9-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e04d9-124">-VaultId</span></span>
<span data-ttu-id="e04d9-125">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="e04d9-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e04d9-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e04d9-126">-Confirm</span></span>
<span data-ttu-id="e04d9-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e04d9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04d9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04d9-128">-WhatIf</span></span>
<span data-ttu-id="e04d9-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e04d9-129">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="e04d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04d9-130">CommonParameters</span></span>
<span data-ttu-id="e04d9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e04d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04d9-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e04d9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04d9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e04d9-133">INPUTS</span></span>

### <span data-ttu-id="e04d9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e04d9-134">System.String</span></span>

## <span data-ttu-id="e04d9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e04d9-135">OUTPUTS</span></span>

### <span data-ttu-id="e04d9-136">BackupEngineBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="e04d9-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="e04d9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e04d9-137">NOTES</span></span>

## <span data-ttu-id="e04d9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e04d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="e04d9-139">AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e04d9-139">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

