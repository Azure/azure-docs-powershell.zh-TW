---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 7612a816db41e3befb58cc739bcc78e2d27ec8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446083"
---
# <span data-ttu-id="800f3-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="800f3-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="800f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="800f3-102">SYNOPSIS</span></span>
<span data-ttu-id="800f3-103">從保存庫登出 SCDPM 服務器或備份伺服器。</span><span class="sxs-lookup"><span data-stu-id="800f3-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="800f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="800f3-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="800f3-105">DESCRIPTION</span></span>
<span data-ttu-id="800f3-106">[ **登出 AzureRmRecoveryServicesBackupManagementServer** ] Cmdlet 會從保存庫中登出) 伺服器或 Azure 備份伺服器的系統中心資料保護管理員 (SCDPM。</span><span class="sxs-lookup"><span data-stu-id="800f3-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="800f3-107">這個 Cmdlet 會移除未從保存庫中登出之伺服器的參考。</span><span class="sxs-lookup"><span data-stu-id="800f3-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="800f3-108">在您可以取消註冊容器之前，您必須刪除所有與該容器相關聯的受保護資料。</span><span class="sxs-lookup"><span data-stu-id="800f3-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="800f3-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="800f3-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="800f3-110">示例</span><span class="sxs-lookup"><span data-stu-id="800f3-110">EXAMPLES</span></span>

### <span data-ttu-id="800f3-111">範例1：從保存庫登出 SCDPM 服務器</span><span class="sxs-lookup"><span data-stu-id="800f3-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="800f3-112">第一個命令會取得名為 dpmserver01.contoso.com 的備份管理伺服器，然後將它儲存在 $BMS 變數中。</span><span class="sxs-lookup"><span data-stu-id="800f3-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="800f3-113">第二個命令會從保存庫登出 SCDPM 服務器。</span><span class="sxs-lookup"><span data-stu-id="800f3-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="800f3-114">參數</span><span class="sxs-lookup"><span data-stu-id="800f3-114">PARAMETERS</span></span>

### <span data-ttu-id="800f3-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="800f3-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="800f3-116">指定要取消註冊的 SCDPM 服務器物件。</span><span class="sxs-lookup"><span data-stu-id="800f3-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="800f3-117">若要取得 **BackupManagementServer** 物件，請使用 Get-AzureRmRecoveryServicesBackupManagementServer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="800f3-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800f3-118">-DefaultProfile</span></span>
<span data-ttu-id="800f3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="800f3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="800f3-120">-PassThru</span></span>
<span data-ttu-id="800f3-121">傳回要刪除的備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="800f3-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="800f3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="800f3-122">-Confirm</span></span>
<span data-ttu-id="800f3-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="800f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800f3-124">-WhatIf</span></span>
<span data-ttu-id="800f3-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="800f3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="800f3-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="800f3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800f3-127">CommonParameters</span></span>
<span data-ttu-id="800f3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="800f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800f3-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="800f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800f3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="800f3-130">INPUTS</span></span>

### <span data-ttu-id="800f3-131">所有</span><span class="sxs-lookup"><span data-stu-id="800f3-131">None</span></span>
<span data-ttu-id="800f3-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="800f3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="800f3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="800f3-133">OUTPUTS</span></span>

## <span data-ttu-id="800f3-134">筆記</span><span class="sxs-lookup"><span data-stu-id="800f3-134">NOTES</span></span>

## <span data-ttu-id="800f3-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="800f3-135">RELATED LINKS</span></span>

[<span data-ttu-id="800f3-136">AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="800f3-136">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


